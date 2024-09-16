---
layout: page
title: Tool Setup Hacks
permalink: /tools/
---

<style>
  ul {
    list-style-type: none;
  }
  li {
    margin-bottom: 1rem;
    font-family: Arial, sans-serif;
  }
  li:before {
    content: "➜ ";
    color: #3498db;
  }
  .command-name {
    font-weight: bold;
    color: #e74c3c;
  }
  .command-desc {
    font-style: italic;
    color: #2c3e50;
  }
</style>

# Shell Commands

<ul>
  <li>
    <span class="command-name">wsl</span>: 
    <span class="command-desc">Launches the Windows Subsystem for Linux (WSL) or accesses a WSL instance. This allows you to run a Linux distribution on Windows.</span>
  </li>

  <li>
    <span class="command-name">cd</span>: 
    <span class="command-desc">Changes the current directory. You use <code>cd &lt;directory&gt;</code> to navigate through different folders.</span>
  </li>

  <li>
    <span class="command-name">git</span>: 
    <span class="command-desc">A version control tool used to clone repositories, commit changes, push/pull code, and collaborate with others.</span>
    <ul>
      <li><code>git clone &lt;repository-url&gt;</code>: Clones a repository.</li>
      <li><code>git commit -m "message"</code>: Commits changes with a message.</li>
      <li><code>git push</code>: Pushes changes to the remote repository.</li>
    </ul>
  </li>

  <li>
    <span class="command-name">apt</span>: 
    <span class="command-desc">A package manager for Ubuntu and Debian-based systems. It is used to install, update, and remove software packages.</span>
    <ul>
      <li><code>sudo apt update</code>: Updates the list of available packages.</li>
      <li><code>sudo apt install &lt;package&gt;</code>: Installs a specified package.</li>
      <li><code>sudo apt upgrade</code>: Upgrades installed packages.</li>
    </ul>
  </li>

  <li>
    <span class="command-name">brew</span>: 
    <span class="command-desc">A package manager for macOS (and Linux, with Homebrew). It helps install software packages.</span>
    <ul>
      <li><code>brew install &lt;package&gt;</code>: Installs a specified package.</li>
      <li><code>brew update</code>: Updates Homebrew to the latest version.</li>
    </ul>
  </li>

  <li>
    <span class="command-name">ls</span>: 
    <span class="command-desc">Lists the contents of the current directory.</span>
    <ul>
      <li><code>ls -l</code>:d Lists details like permissions, owner, and modification date.</li>
    </ul>
  </li>

  <li>
    <span class="command-name">mkdir</span>: 
    <span class="command-desc">Creates a new directory. Example: <code>mkdir &lt;directory-name&gt;</code>.</span>
  </li>

  <li>
    <span class="command-name">rm</span>: 
    <span class="command-desc">Removes files or directories.</span>
    <ul>
      <li><code>rm &lt;file&gt;</code>: Removes a file.</li>
      <li><code>rm -r &lt;directory&gt;</code>: Removes a directory and its contents.</li>
    </ul>
  </li>

  <li>
    <span class="command-name">mv</span>: 
    <span class="command-desc">Moves or renames files or directories. Example: <code>mv &lt;old-file&gt; &lt;new-file&gt;</code> to rename a file.</span>
  </li>

  <li>
    <span class="command-name">cp</span>: 
    <span class="command-desc">Copies files or directories. Example: <code>cp &lt;source&gt; &lt;destination&gt;</code>.</span>
  </li>

  <li>
    <span class="command-name">sudo</span>: 
    <span class="command-desc">Executes a command with superuser (admin) privileges. For example, <code>sudo apt install &lt;package&gt;</code> gives admin access to install the software.</span>
  </li>

  <li>
    <span class="command-name">cat</span>: 
    <span class="command-desc">Displays the contents of a file. Example: <code>cat &lt;file&gt;</code> to read a file in the terminal.</span>
  </li>
</ul>


<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  h1, h2 {
    color: #2c3e50;
  }
  code {
    background-color: #f4f4f4;
    border-radius: 3px;
    padding: 0.2em 0.4em;
    color: #e74c3c;
    font-family: Consolas, monospace;
  }
  .step {
    margin-bottom: 1.2rem;
  }
  .command {
    background-color: #ecf0f1;
    padding: 0.5em;
    border-radius: 3px;
    color: #2980b9;
    display: inline-block;
    margin-bottom: 0.5em;
  }
</style>
---

# Version Control

## 1. What have you learned about version control during this setup process?

During this setup process, I learned that version control, specifically using Git and GitHub, is a system that tracks changes to files and manages versions over time. Version control allows multiple developers to collaborate efficiently on a project and maintain a history of all changes. Some key takeaways include:

- **Git** is a version control system that operates locally on your machine.
- **GitHub** is an online platform for hosting Git repositories and collaborating with others.

## 2. How are the files from GitHub placed on your local machine? How do you navigate to those files?

To download files from GitHub onto your local machine, use the following steps:

### Step-by-step:

<div class="step">
  <div class="command">git clone &lt;repository-url&gt;</div>
  This command copies the repository from GitHub to your local machine.
</div>

<div class="step">
  <div class="command">cd &lt;repository-folder&gt;</div>
  Use this command to navigate into the cloned folder.
</div>

Once inside the folder, you can start working on the files using your editor.

## 3. How are the files updated in GitHub? How do you navigate to those files?

To update the files in GitHub after making changes locally, follow this sequence of commands:

### Step-by-step:

<div class="step">
  <div class="command">git add &lt;file-name&gt;</div>
  Stage the modified files for commit.
</div>

<div class="step">
  <div class="command">git commit -m "Description of changes"</div>
  Commit your changes with a message that describes the updates.
</div>

<div class="step">
  <div class="command">git push origin main</div>
  Push the changes to GitHub, updating the remote repository.
</div>

To navigate to your repository on GitHub, go to `https://github.com/your-username/repository-name`.

## 4. How would you update your template of the `portfolio_2025` repository? How would you make it more applicable to your specific course?

To update the `portfolio_2025` repository and customize it for your course, you can follow these steps:

### Step-by-step:

1. **Clone the repository** if you haven't already:
   <div class="command">git clone &lt;portfolio_2025-repo-url&gt;</div>

2. **Navigate to the repository folder**:
   <div class="command">cd portfolio_2025</div>

3. **Customize the template**:
   - **Change content**: Update the text, images, and structure to reflect your course.
   - **Modify styles**: Update CSS files to change colors, fonts, and layout for a more personalized design.
   - **Add course materials**: Include specific files related to your course (assignments, notes, etc.).

4. **Commit and push changes** to GitHub:
   <div class="command">git add .</div>  
   <div class="command">git commit -m "Updated portfolio for course"</div>  
   <div class="command">git push origin main</div>

Your portfolio will now be updated on GitHub with your customized changes!
---

<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  h2 {
    color: #2c3e50;
  }
  .url {
    background-color: #f4f4f4;
    padding: 0.2em 0.4em;
    border-radius: 3px;
    color: #3498db;
    font-family: Consolas, monospace;
  }
  p {
    margin-bottom: 1.2rem;
  }
</style>
---
## Difference between Localhost and Deployed Server
<p>
Localhost is for development on my personal machine, and only I can access it. 
When deployed on a server like GitHub Pages, the project becomes publicly accessible on the internet, 
and anyone with the URL can view it.
</p>

## Localhost URL
<p>
My project's localhost URL is <span class="url">http://127.0.0.1:4100/vibha_mandayam_2025/</span>. 
No one else can access this unless they are on my network.
</p>

## GitHub Pages URL
<p>
My GitHub Pages URL is <span class="url">https://vibha1019.github.io/vibha_mandayam_2025/</span>. 
Yes, anyone with the link can view the site.
</p>
---
<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  h2 {
    color: #2c3e50;
  }
  .url {
    background-color: #f4f4f4;
    padding: 0.2em 0.4em;
    border-radius: 3px;
    color: #3498db;
    font-family: Consolas, monospace;
  }
  p {
    margin-bottom: 1.2rem;
  }
</style>

## DNS and GitHub Pages

### 1. Domain on GitHub Pages:

<p>
Yes, the default domain provided by GitHub Pages is 
<span class="url">https://your-username.github.io/repository-name/</span>.
</p>

### 2. Different URL from neighbors:

<p>
Yes, each GitHub Pages URL is different based on the GitHub username and repository name. 
I haven’t changed the URL, but if I purchase a custom domain, I could update it by configuring my DNS settings.
</p>
---

<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  h2 {
    color: #2c3e50;
  }
  .command {
    background-color: #f4f4f4;
    padding: 0.2em 0.4em;
    border-radius: 3px;
    color: #3498db;
    font-family: Consolas, monospace;
    display: inline-block;
  }
  p {
    margin-bottom: 1.2rem;
  }
  .issue {
    background-color: #ecf0f1;
    border-left: 4px solid #e74c3c;
    padding: 0.5em;
    margin-bottom: 1.2rem;
  }
  .resolution {
    background-color: #eafaf1;
    border-left: 4px solid #2ecc71;
    padding: 0.5em;
    margin-bottom: 1.2rem;
  }
</style>

<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  h2 {
    color: #2c3e50;
  }
  .command {
    background-color: #f4f4f4;
    padding: 0.2em 0.4em;
    border-radius: 3px;
    color: #3498db;
    font-family: Consolas, monospace;
    display: inline-block;
  }
  p {
    margin-bottom: 1.2rem;
  }
  .section {
    margin-bottom: 2rem;
  }
  .issue {
    background-color: #ecf0f1;
    border-left: 4px solid #e74c3c;
    padding: 0.5em;
    margin-bottom: 1.2rem;
  }
  .resolution {
    background-color: #eafaf1;
    border-left: 4px solid #2ecc71;
    padding: 0.5em;
    margin-bottom: 1.2rem;
  }
</style>
---
## Verify Installation
While I had prior experience with **VSCode** and using **GitHub**, I encountered some challenges when trying to open my repositories with **WSL**.

### Installation Issue

I ran into an error while attempting to install the script:

```bash
scripts/venv.sh

# Activate virtual environment, observe prompt change after running it
source venv/bin/activate

``` 

To solve the issue, I had to properly install Python 3, as I was having some troubles with that. However, by following the steps given in the command output, the problem was fixed.
---

