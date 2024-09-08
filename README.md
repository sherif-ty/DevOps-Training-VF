<h1>Linux Commands</h1>
<p></p>
<img src="https://drive.google.com/uc?export=view&id=1CT-CujN16EmPUY6_3xfaHDz352DLVI2s" alt="Linux Virtual Machine Access via SSH" width="500">
<p></p>

<h2>Vagrant Linux Machine Setup</h2>

<p>This guide explains how to set up a small Linux machine using Vagrant and VirtualBox, and how to access it as the root user via PuTTY.</p>

<h2>Steps to Set Up the Vagrant Machine</h2>

<ol>
  <li>
    <pre><code>1-Make sure you are on 2-Linux-Commands branch on you local machine.</code></pre>
  </li>
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
