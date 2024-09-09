<h1>Linux Commands</h1>
<p></p>
<img src="https://drive.google.com/uc?export=view&id=1CT-CujN16EmPUY6_3xfaHDz352DLVI2s" alt="Linux Virtual Machine Access via SSH" width="500">
<p></p>

<h2>Vagrant Linux Machine Setup</h2>

<p>This guide explains how to set up a small Linux machine using Vagrant and VirtualBox, and how to access it as the root user via PuTTY.</p>

<h2>Steps to Set Up the Vagrant Machine</h2>

<ol>
  <li>1-Make sure you are on 2-Linux-Commands branch on your local machine.</li>
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

<h1>Learning Linux Basic Commands</h1>

<p>This session introduces basic Linux commands and covers working with permissions, files, and text editors. It’s perfect for beginners looking to gain familiarity with Linux terminal operations.</p>

<h2><button onclick="toggleDropdown('nav-filesystem')">1. Navigating the Filesystem</button></h2>
<div id="nav-filesystem" style="display:none;">
  <ul>
    <li><strong>List files and directories:</strong> 
      <pre><code>ls</code></pre>
    </li>
    <li><strong>Change directory:</strong> 
      <pre><code>cd /path/to/directory</code></pre>
    </li>
    <li><strong>Print the current directory:</strong> 
      <pre><code>pwd</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('manage-files')">2. Managing Files and Directories</button></h2>
<div id="manage-files" style="display:none;">
  <ul>
    <li><strong>Create a directory:</strong> 
      <pre><code>mkdir mydir</code></pre>
    </li>
    <li><strong>Create an empty file:</strong> 
      <pre><code>touch myfile.txt</code></pre>
    </li>
    <li><strong>Copy files:</strong> 
      <pre><code>cp source.txt destination.txt</code></pre>
    </li>
    <li><strong>Move/rename files:</strong> 
      <pre><code>mv oldname.txt newname.txt</code></pre>
    </li>
    <li><strong>Remove files:</strong> 
      <pre><code>rm myfile.txt</code></pre>
    </li>
    <li><strong>Remove directories:</strong> 
      <pre><code>rm -r mydir</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('permissions')">3. File Permissions</button></h2>
<div id="permissions" style="display:none;">
  <p>Each file or directory in Linux has associated permissions that define read, write, and execute rights.</p>
  <ul>
    <li><strong>View file permissions:</strong> 
      <pre><code>ls -l</code></pre>
    </li>
    <li><strong>Change file permissions:</strong> 
      <pre><code>chmod 755 myfile.txt</code></pre>
    </li>
    <li><strong>Change file ownership:</strong> 
      <pre><code>chown user:group myfile.txt</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('text-editors')">4. Working with Text Editors</button></h2>
<div id="text-editors" style="display:none;">
  <ul>
    <li><strong>Edit a file with Nano:</strong> 
      <pre><code>nano myfile.txt</code></pre>
    </li>
    <li><strong>Edit a file with Vim:</strong> 
      <pre><code>vim myfile.txt</code></pre>
      <p>To insert text, press <code>i</code> to enter insert mode, then type. Press <code>ESC</code> and type <code>:wq</code> to save and quit.</p>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('find-files')">5. Searching and Finding Files</button></h2>
<div id="find-files" style="display:none;">
  <ul>
    <li><strong>Find files:</strong> 
      <pre><code>find /path -name "filename"</code></pre>
    </li>
    <li><strong>Search within files (using grep):</strong> 
      <pre><code>grep "pattern" filename</code></pre>
    </li>
    <li><strong>Search recursively in directories (using grep):</strong> 
      <pre><code>grep -r "pattern" /path/to/directory</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('process-management')">6. Process Management</button></h2>
<div id="process-management" style="display:none;">
  <ul>
    <li><strong>View running processes:</strong> 
      <pre><code>ps aux</code></pre>
    </li>
    <li><strong>Kill a process by ID:</strong> 
      <pre><code>kill 1234</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('network')">7. Network Commands</button></h2>
<div id="network" style="display:none;">
  <ul>
    <li><strong>Check network interface details:</strong> 
      <pre><code>ifconfig</code></pre>
    </li>
    <li><strong>Ping a host:</strong> 
      <pre><code>ping google.com</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('compression')">8. File Compression and Decompression</button></h2>
<div id="compression" style="display:none;">
  <ul>
    <li><strong>Compress files:</strong> 
      <pre><code>tar -czvf archive.tar.gz /path/to/folder</code></pre>
    </li>
    <li><strong>Decompress files:</strong> 
      <pre><code>tar -xzvf archive.tar.gz</code></pre>
    </li>
  </ul>
</div>

<h2><button onclick="toggleDropdown('history')">9. Command History</button></h2>
<div id="history" style="display:none;">
  <ul>
    <li><strong>View the command history:</strong> 
      <pre><code>history</code></pre>
    </li>
    <li><strong>Rerun a command from history by its number:</strong> 
      <pre><code>!123</code></pre>
    </li>
  </ul>
</div>

<h2>Learning Resources</h2>
<ul>
  <li><a href="https://medium.com/" target="_blank">Linux Basics: Medium Learning Resources</a></li>
</ul>

<script>
  function toggleDropdown(id) {
    var element = document.getElementById(id);
    if (element.style.display === "none") {
      element.style.display = "block";
    } else {
      element.style.display = "none";
    }
  }
</script>
