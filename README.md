<h2>Learning Docker</h2>

<h3>Docker Linux Machine Setup</h3>
<p>This guide explains how to set up a small Linux container using Docker and interact with it via a terminal on your local machine.</p>

<h3>Steps to Set Up a Docker Container</h3>

<ol>
    <li>Ensure Docker is installed on your local machine. Verify with:</li>
    <pre><code>docker --version</code></pre>

    <li>To pull the latest Ubuntu image from Docker Hub:</li>
    <pre><code>docker pull ubuntu:latest</code></pre>

    <li>Run a new container based on the Ubuntu image:</li>
    <pre><code>docker run -it --name my-ubuntu-container ubuntu</code></pre>

    <li>List all running containers:</li>
    <pre><code>docker ps</code></pre>

    <li>Stop a running container:</li>
    <pre><code>docker stop my-ubuntu-container</code></pre>

    <li>Start the container again:</li>
    <pre><code>docker start my-ubuntu-container</code></pre>

    <li>Execute a command within the container (e.g., bash shell):</li>
    <pre><code>docker exec -it my-ubuntu-container bash</code></pre>

    <li>Remove a container once it's stopped:</li>
    <pre><code>docker rm my-ubuntu-container</code></pre>
</ol>

<h3>Using a Dockerfile</h3>
<p>In Docker, a <strong>Dockerfile</strong> is a script that contains a series of instructions for building a Docker image. Below is an example Dockerfile to set up a basic web server using Nginx.</p>

<h4>Steps to Create and Use a Dockerfile</h4>
<ol>
    <li>Create a new directory for your Docker project and navigate into it:</li>
    <pre><code>mkdir my-docker-app && cd my-docker-app</code></pre>

    <li>Create a <strong>Dockerfile</strong> with the following content:</li>
    <pre><code>
# Use the official Nginx image from Docker Hub
FROM nginx:latest

# Copy a custom index.html to the container
COPY ./index.html /usr/share/nginx/html/index.html

# Expose port 80 to the host machine
EXPOSE 80
    </code></pre>

    <li>Create an <strong>index.html</strong> file in the same directory:</li>
    <pre><code>&lt;html&gt;
&lt;head&gt;&lt;title&gt;My Docker App&lt;/title&gt;&lt;/head&gt;
&lt;body&gt;&lt;h1&gt;Hello from Docker!&lt;/h1&gt;&lt;/body&gt;
&lt;/html&gt;</code></pre>

    <li>Build the Docker image from the Dockerfile:</li>
    <pre><code>docker build -t my-nginx-app .</code></pre>

    <li>Run the Docker container using the image you just built:</li>
    <pre><code>docker run -d -p 8080:80 my-nginx-app</code></pre>

    <li>Open a browser and navigate to <code>http://localhost:8080</code>. You should see your custom HTML page!</li>
</ol>

<h3>Connecting to the Docker Container Using Terminal</h3>
<p>Once the container is running, you can connect to it via the terminal:</p>
<ul>
    <li>Find the container’s IP address with:</li>
    <pre><code>docker inspect my-nginx-app | grep IPAddress</code></pre>
    <li>Username: <code>root</code></li>
    <li>Password: Not required for root access within Docker containers.</li>
</ul>

<h3>Notes</h3>
<ul>
    <li>The container uses a minimal setup with Nginx as the base web server.</li>
    <li>You can customize the <strong>Dockerfile</strong> to install additional software or services in the container.</li>
</ul>

<h3>Learning Docker Basic Commands</h3>
<p>This session introduces basic Docker commands and covers container management, image handling, and networking. It’s perfect for beginners looking to gain familiarity with Docker operations.</p>

<h4>1. Working with Images</h4>
<pre><code>docker images</code></pre>
<p>Lists all Docker images on your system.</p>

<h4>2. Pull an Image</h4>
<pre><code>docker pull &lt;image_name&gt;</code></pre>
<p>Pulls the specified image from Docker Hub.</p>

<h4>3. Running a Container</h4>
<pre><code>docker run -it &lt;image_name&gt;</code></pre>
<p>Creates and starts a new container based on the specified image.</p>

<h4>4. Listing Containers</h4>
<pre><code>docker ps</code></pre>
<p>Shows all running containers.</p>

<h4>5. Stopping a Container</h4>
<pre><code>docker stop &lt;container_name&gt;</code></pre>
<p>Stops the specified running container.</p>

<h4>6. Removing a Container</h4>
<pre><code>docker rm &lt;container_name&gt;</code></pre>
<p>Deletes the specified container once it is stopped.</p>

<h4>7. Viewing Logs</h4>
<pre><code>docker logs &lt;container_name&gt;</code></pre>
<p>Displays the logs of the specified container.</p>

<h4>8. Inspecting a Container</h4>
<pre><code>docker inspect &lt;container_name&gt;</code></pre>
<p>Provides detailed information about the specified container, including IP addresses, configuration, and state.</p>

<h3>Learning Resources</h3>
<ul>
    <li><a href="https://docs.docker.com/get-started/" target="_blank">Docker Official Documentation</a> - Comprehensive guide on Docker installation, setup, and usage.</li>
    <li><a href="https://www.udemy.com/course/docker-mastery/" target="_blank">Docker Mastery on Udemy</a> - In-depth course covering Docker fundamentals.</li>
    <li><a href="https://www.youtube.com/watch?v=fqMOX6JJhGo" target="_blank">Docker Tutorial for Beginners (YouTube)</a> - A popular video tutorial covering Docker basics.</li>
    <li><a href="https://docker-curriculum.com/" target="_blank">Docker Curriculum</a> - A beginner-friendly guide for learning Docker step by step.</li>
</ul>

<h3>Conclusion</h3>
<p>These basic Docker commands will help you get started with container management. As you continue, explore more advanced Docker topics like networking, volumes, and Docker Compose. Use the resources provided to enhance your knowledge.</p>
