<h1>Git Commands</h1>
<p></p>
<img src="https://drive.google.com/uc?export=view&id=1UB5IJy7YOxoJ3x9HxymR7cUEXUnuTN4B" alt="Google Drive File" width="500">
<p></p>

<h1>Vagrant Linux Machine Setup with GitLab</h1>

<p>This guide explains how to set up a small Linux machine using Vagrant and VirtualBox, and how to access it as the root user via PuTTY and access the GitLab container from your local machine.</p>

<h2>Steps to Set Up the Vagrant Machine</h2>

<ol>
  <li>1-Make sure you are on the correct branch for your Vagrant setup.</li>
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

<h2>Accessing the GitLab Container</h2>

<ol>
  <li>After the Vagrant machine is up and running, open your web browser.</li>
  <li>In the browser's address bar, enter:
    <pre><code>http://192.168.56.10</code></pre>
  </li>
  <li>GitLab should now be accessible through your browser.</li>
  <li>You can also SSH into the GitLab container via your terminal:
    <pre><code>ssh git@192.168.56.10</code></pre>
  </li>
</ol>

<h2>Notes</h2>
<ul>
  <li>The GitLab container will be available on port 80 for HTTP access and port 22 for SSH access.</li>
  <li>Modify the IP address or other configurations by editing the <code>Vagrantfile</code> if needed.</li>
</ul>
