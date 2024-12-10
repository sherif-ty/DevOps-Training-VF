<h1 align="center">CICD with Jenkins Training</h1>

<p align="center">
<img src="https://drive.google.com/uc?export=view&id=1j6BQf9eHSuEqFtWaQJ023ARETz2dl17a" alt="CICD with Jenkins" />

</p>

<h2>Introduction</h2>
<p>
  Continuous Integration (CI) and Continuous Deployment (CD) are practices that improve software development by automating integration and deployment processes. 
  Jenkins, an open-source automation server, is widely used for implementing CI/CD pipelines due to its robust plugin ecosystem and ease of use.
</p>

<h3>What are CI and CD?</h3>
<ul>
  <li>
    <strong>Continuous Integration (CI):</strong> Merging developers' working copies to a shared mainline frequently, aiming to detect and address errors quickly.
  </li>
  <li>
    <strong>Continuous Deployment (CD):</strong> Automatically deploying changes that pass all stages of your production pipeline, ensuring software can be released to production anytime.
  </li>
</ul>

<h3>Why Jenkins?</h3>
<ul>
  <li><strong>Extensibility:</strong> Over 1800 plugins for integration with various tools and services.</li>
  <li><strong>Community Support:</strong> A large, active community contributing to its development.</li>
  <li><strong>Ease of Use:</strong> User-friendly interface and comprehensive documentation.</li>
</ul>

<h2>Training Sessions</h2>
<ol>
  <li><strong>Introduction to CICD:</strong> Overview of Continuous Integration and Continuous Deployment.</li>
  <li><strong>Setting Up Jenkins:</strong> Installing and configuring Jenkins, understanding the interface.</li>
  <li><strong>Automating Builds:</strong> Integrating version control systems and setting up build jobs.</li>
  <li><strong>Integrating Docker:</strong> Using Docker containers as Jenkins build agents.</li>
  <li><strong>Designing Pipelines:</strong> Creating declarative and scripted pipelines using Jenkinsfiles.</li>
  <li><strong>Deploying Applications:</strong> Automating deployment strategies like rolling updates and blue-green deployments.</li>
  <li><strong>Monitoring Jobs:</strong> Monitoring job execution using plugins and logs.</li>
  <li><strong>Advanced Topics (Optional):</strong> Securing Jenkins, cloud integrations, and custom plugins.</li>
</ol>

<h2>Pipeline Configuration Tips</h2>
<ul>
  <li>
    <strong>Pre Actions:</strong> Use options like "Abort the build if it’s stuck" and "Add timestamps to the Console Output."
  </li>
  <li>
    <strong>Post Actions:</strong> Add actions like "Archive the artifacts" or "Send build notifications."
  </li>
</ul>

<h2>Triggers</h2>
<ul>
  <li>
    <strong>Poll SCM:</strong> Automate builds using Cron syntax (e.g., every 5 minutes: <code>H/5 * * * *</code>).
  </li>
  <li>
    <strong>GitHub Push Trigger:</strong> Configure a webhook in GitHub to trigger Jenkins builds automatically.
  </li>
</ul>

<h2>Reference</h2>
<p>
  For detailed steps, visit the original article: 
  <a href="https://medium.com/@sharma0purnima/how-to-set-up-ci-cd-using-jenkins-8e17685136e7" target="_blank">
    How to Set Up CI/CD Using Jenkins
  </a>
</p>
