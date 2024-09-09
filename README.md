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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Git Commands</title>
</head>
<body>
    <h1>Learning Git Commands</h1>
    
    <h2>Introduction</h2>
    <p>Git is a version control system that allows you to track changes to your codebase and collaborate with others. Here’s a guide to some essential Git commands.</p>
    
    <h2>Basic Git Commands</h2>
    
    <h3>1. Initialize a New Repository</h3>
    <pre><code>git init</code></pre>
    <p>Creates a new Git repository in the current directory.</p>
    
    <h3>2. Clone a Repository</h3>
    <pre><code>git clone &lt;repository_url&gt;</code></pre>
    <p>Creates a local copy of a remote repository.</p>
    
    <h3>3. Check Repository Status</h3>
    <pre><code>git status</code></pre>
    <p>Displays the state of the working directory and the staging area.</p>
    
    <h3>4. Add Changes to Staging Area</h3>
    <pre><code>git add &lt;file_name&gt;</code></pre>
    <p>Adds changes from a specific file to the staging area. Use <code>git add .</code> to add all changes.</p>
    
    <h3>5. Commit Changes</h3>
    <pre><code>git commit -m "Commit message"</code></pre>
    <p>Saves the changes in the staging area to the repository with a descriptive message.</p>
    
    <h3>6. View Commit History</h3>
    <pre><code>git log</code></pre>
    <p>Displays a list of commits in the repository.</p>
    
    <h3>7. Create a New Branch</h3>
    <pre><code>git branch &lt;branch_name&gt;</code></pre>
    <p>Creates a new branch in the repository.</p>
    
    <h3>8. Switch Branches</h3>
    <pre><code>git checkout &lt;branch_name&gt;</code></pre>
    <p>Switches to the specified branch.</p>
    
    <h3>9. Merge Branches</h3>
    <pre><code>git merge &lt;branch_name&gt;</code></pre>
    <p>Merges the specified branch into the current branch.</p>
    
    <h3>10. Push Changes to Remote Repository</h3>
    <pre><code>git push origin &lt;branch_name&gt;</code></pre>
    <p>Uploads changes from the local repository to the remote repository.</p>
    
    <h3>11. Pull Changes from Remote Repository</h3>
    <pre><code>git pull origin &lt;branch_name&gt;</code></pre>
    <p>Fetches and merges changes from the remote repository to the local repository.</p>
    
    <h2>Learning Resources</h2>
    <ul>
        <li><a href="https://git-scm.com/doc" target="_blank">Git Documentation</a> - Official documentation with comprehensive details about Git commands and usage.</li>
        <li><a href="https://www.atlassian.com/git/tutorials/what-is-git" target="_blank">Atlassian Git Tutorials</a> - Tutorials covering Git basics and advanced topics.</li>
        <li><a href="https://www.codecademy.com/learn/learn-git" target="_blank">Codecademy Git Course</a> - Interactive course for learning Git from scratch.</li>
        <li><a href="https://www.udemy.com/course/git-and-github-bootcamp/" target="_blank">Udemy Git and GitHub Bootcamp</a> - In-depth course on Git and GitHub.</li>
        <li><a href="https://www.youtube.com/watch?v=8JJ101D3knE" target="_blank">Git Tutorial for Beginners (YouTube)</a> - Video tutorial covering Git basics.</li>
    </ul>
    
    <h2>Conclusion</h2>
    <p>These are some of the basic Git commands you will use frequently. Mastering these will help you efficiently manage your codebase and collaborate with others. Utilize the resources provided to deepen your understanding of Git.</p>
</body>
</html>
