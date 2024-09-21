Vagrant.configure("2") do |config|
  
  # Define the base box to use
  config.vm.box = "ubuntu/bionic64"  # Minimal Ubuntu 18.04 (Bionic Beaver)
  
  # Assign a static IP
  config.vm.network "private_network", ip: "192.168.56.10"
  
  # Set minimal VM specifications
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"  # 512 MB of RAM
    vb.cpus = 1        # 1 CPU
  end

  # Configure SSH access with a password
  config.vm.provider "virtualbox" do |vbox|
    vbox.customize ["modifyvm", :id, "--natpf1", "guestssh,tcp,,2222,,22"]
  end

  # Set root user and password for SSH
  config.vm.provision "shell", inline: <<-SHELL
    echo root:password | sudo chpasswd
    sudo sed -i 's/^#PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config
    sudo sed -i 's/^PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
    sudo service ssh restart
  SHELL

end
