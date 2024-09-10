<h1>Learning Docker</h1>
<p></p>
<a href="https://drive.google.com/file/d/181ia-CO4ZVMCG63kzIPsib01xTkMNkP3/view?usp=sharing" target="_blank">
    <img src="https://drive.google.com/uc?export=view&id=181ia-CO4ZVMCG63kzIPsib01xTkMNkP3" alt="Learning Docker" width="500">
</a>
<p></p>

<h2>Vagrant Linux Machine Setup</h2>

<p>This guide explains how to set up a small Linux machine using Vagrant and VirtualBox, and how to access it as the root user via PuTTY.</p>

<h2>Steps to Set Up the Vagrant Machine</h2>

<ol>
  <li>1-Make sure you are on 4-learning docker branch on your local machine.</li>
  <li>If the machine is already running, reload it with provisioning to apply the new configuration:
    <pre><code>vagrant reload --provision</code></pre>
  </li>
  <li>Start the Vagrant machine:
    <pre><code>vagrant up</code></pre>
  </li>
  <li>To check the SSH configuration of the machine:
    <pre><code>vagrant ssh-config</code></pre>
  </li>
</ol>

<h2>Connecting to the Linux Machine Using PuTTY</h2>

<ol>
  <li>Open PuTTY and set the following configuration:
    <ul>
      <li><strong>IP address:</strong> <code>192.168.56.10</code></li>
      <li><strong>Port:</strong> <code>22</code></li>
      <li><strong>Username:</strong> <code>root</code></li>
      <li><strong>Password:</strong> <code>password</code></li>
    </ul>
  </li>
  <li>Click <strong>Open</strong> to initiate the connection. You will now be able to log into the Linux machine as <code>root</code>.</li>
</ol>

<h2>Notes</h2>
<ul>
  <li>The machine uses a minimal setup with Ubuntu as the base operating system.</li>
  <li>The machine is configured to allow <code>root</code> access with password authentication via SSH.</li>
  <li>You can modify the IP address or resource allocation (memory and CPU) by editing the <code>Vagrantfile</code>.</li>
</ul>

<h2>Learning Docker Commands</h2>

<p>This session covers essential Docker commands to help you manage containers, images, and networks in Docker.</p>

<h3>1. Docker Installation</h3>
<p>Ensure Docker is installed on your system by running:</p>
<pre><code>docker --version</code></pre>

<h3>2. Pulling Docker Images</h3>
<p>To download an image from Docker Hub, use:</p>
<pre><code>docker pull &lt;image_name&gt;</code></pre>
<p>Example:</p>
<pre><code>docker pull ubuntu:latest</code></pre>

<h3>3. Listing Docker Images</h3>
<p>View all images stored on your system with:</p>
<pre><code>docker images</code></pre>

<h3>4. Running a Docker Container</h3>
<p>To create and start a new container based on an image:</p>
<pre><code>docker run -it &lt;image_name&gt;</code></pre>
<p>Example:</p>
<pre><code>docker run -it ubuntu bash</code></pre>

<h3>5. Listing Running Containers</h3>
<p>Check all currently running containers with:</p>
<pre><code>docker ps</code></pre>

<h3>6. Stopping a Running Container</h3>
<p>To stop a specific container:</p>
<pre><code>docker stop &lt;container_name_or_id&gt;</code></pre>

<h3>7. Restarting a Stopped Container</h3>
<p>Start a stopped container again:</p>
<pre><code>docker start &lt;container_name_or_id&gt;</code></pre>

<h3>8. Removing a Docker Container</h3>
<p>Once the container is stopped, remove it with:</p>
<pre><code>docker rm &lt;container_name_or_id&gt;</code></pre>

<h3>9. Viewing Logs of a Container</h3>
<p>To see the logs of a specific container:</p>
<pre><code>docker logs &lt;container_name_or_id&gt;</code></pre>

<h3>10. Docker Container Details</h3>
<p>Inspect detailed information about a container:</p>
<pre><code>docker inspect &lt;container_name_or_id&gt;</code></pre>

<h3>11. Docker Networking</h3>
<p>List all Docker networks:</p>
<pre><code>docker network ls</code></pre>

<h3>12. Removing Docker Images</h3>
<p>To delete an image:</p>
<pre><code>docker rmi &lt;image_name_or_id&gt;</code></pre>

<h3>Learning Resources</h3>
<ul>
    <li><a href="https://docs.docker.com/get-started/" target="_blank">Docker Official Documentation</a></li>
    <li><a href="https://www.docker.com/101-tutorial" target="_blank">Docker 101 Tutorial</a></li>
    <li><a href="https://www.youtube.com/watch?v=fqMOX6JJhGo" target="_blank">Docker Tutorial for Beginners (YouTube)</a></li>
</ul>
