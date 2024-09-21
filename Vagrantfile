Vagrant.configure("2") do |config|
  
  # Define the base box to use
  config.vm.box = "ubuntu/bionic64"  # Minimal Ubuntu 18.04 (Bionic Beaver)
  
  # Assign a static IP
  config.vm.network "private_network", ip: "192.168.56.10"
  
  # Set minimal VM specifications
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4000"  # 4 GB of RAM
    vb.cpus = 1        # 1 CPU
  end

  # Configure SSH access with a password
  config.vm.provider "virtualbox" do |vbox|
    vbox.customize ["modifyvm", :id, "--natpf1", "guestssh,tcp,,2222,,22"]
  end

  # Set root user and password for SSH, and install Docker & GitLab
  config.vm.provision "shell", inline: <<-SHELL
    # Set root password
    echo root:password | sudo chpasswd
    sudo sed -i 's/^#PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config
    sudo sed -i 's/^PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
    sudo service ssh restart

    # Update the system and install Docker
    sudo apt-get update
    sudo apt-get install -y docker.io

    # Start Docker and ensure it runs on boot
    sudo systemctl start docker
    sudo systemctl enable docker

    # Run GitLab container
    sudo docker run --detach \
      --hostname 192.168.56.10 \
      --publish 80:80 --publish 443:443 --publish 2222:22 \
      --name gitlab \
      --restart always \
      --volume /srv/gitlab/config:/etc/gitlab \
      --volume /srv/gitlab/logs:/var/log/gitlab \
      --volume /srv/gitlab/data:/var/opt/gitlab \
      gitlab/gitlab-ce:latest

    # Wait for GitLab to start
    echo "Waiting for GitLab to be ready..."
    sleep 60
  SHELL

  # Port forward so you can access GitLab from the local machine
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 443, host: 8443

end
