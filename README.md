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
<h2>3- Access GitLab: After the VM is up, you can access GitLab on your local machine by navigating to:</h2>

<h3>*HTTP: http://localhost:8080</h3>
<h3>*HTTPS: https://localhost:8443</h3>
<h4>Accessing the GitLab Container ....optional</h4>

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


<h2>Learning Git Commands</h2>

<h3>Introduction</h3>
<p>Git is a version control system that allows you to track changes to your codebase and collaborate with others. Here’s a guide to some essential Git commands.</p>

<h3>Basic Git Commands</h3>

<h4>1. Initialize a New Repository</h4>
<pre><code>git init</code></pre>
<p>Creates a new Git repository in the current directory.</p>

<h4>2. Clone a Repository</h4>
<pre><code>git clone &lt;repository_url&gt;</code></pre>
<p>Creates a local copy of a remote repository.</p>

<h4>3. Check Repository Status</h4>
<pre><code>git status</code></pre>
<p>Displays the state of the working directory and the staging area.</p>

<h4>4. Add Changes to Staging Area</h4>
<pre><code>git add &lt;file_name&gt;</code></pre>
<p>Adds changes from a specific file to the staging area. Use <code>git add .</code> to add all changes.</p>

<h4>5. Commit Changes</h4>
<pre><code>git commit -m "Commit message"</code></pre>
<p>Saves the changes in the staging area to the repository with a descriptive message.</p>

<h4>6. View Commit History</h4>
<pre><code>git log</code></pre>
<p>Displays a list of commits in the repository.</p>

<h4>7. Create a New Branch</h4>
<pre><code>git branch &lt;branch_name&gt;</code></pre>
<p>Creates a new branch in the repository.</p>

<h4>8. Switch Branches</h4>
<pre><code>git checkout &lt;branch_name&gt;</code></pre>
<p>Switches to the specified branch.</p>

<h4>9. Merge Branches</h4>
<pre><code>git merge &lt;branch_name&gt;</code></pre>
<p>Merges the specified branch into the current branch.</p>

<h4>10. Push Changes to Remote Repository</h4>
<pre><code>git push origin &lt;branch_name&gt;</code></pre>
<p>Uploads changes from the local repository to the remote repository.</p>

<h4>11. Pull Changes from Remote Repository</h4>
<pre><code>git pull origin &lt;branch_name&gt;</code></pre>
<p>Fetches and merges changes from the remote repository to the local repository.</p>

<h3>Learning Resources</h3>
<ul>
    <li><a href="https://git-scm.com/doc" target="_blank">Git Documentation</a> - Official documentation with comprehensive details about Git commands and usage.</li>
    <li><a href="https://www.atlassian.com/git/tutorials/what-is-git" target="_blank">Atlassian Git Tutorials</a> - Tutorials covering Git basics and advanced topics.</li>
  
</ul>

<h3>Conclusion</h3>
<p>These are some of the basic Git commands you will use frequently. Mastering these will help you efficiently manage your codebase and collaborate with others. Utilize the resources provided to deepen your understanding of Git.</p>
