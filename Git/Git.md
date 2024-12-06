<h2>What is Git?</h2>

Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work on a project simultaneously without overwriting each other's changes.

<h2>Key Features of Git</h2>

</body>
<p><h3>Distributed System:</h3> Every developer has a full copy of the repository, including its history.</p>
<p> <h3>Branching and Merging:</h3> Git supports powerful branching and merging, allowing you to experiment with new features safely.</p>
<p><h3>Staging Area:</h3> Git has a staging area where you can format and review changes before committing them.</p>
<p><h3>Lightweight:</h3> Git is fast and efficient, making it suitable for large projects.</p>
</body>

<h2>Stages in Git</h2>

In Git, files go through several stages as they move through the version control process. Understanding these stages is crucial for effective version control. 

**Here are the main stages in Git:**

**1. Working Directory**

This is where you make changes to your files. The working directory contains the actual files of your project. When you modify a file, it is in the working directory.

**2. Staging Area (Index)**

The staging area is like a preparation area where you can review and format changes before committing them. You add changes to the staging area using the git add command. This step allows you to selectively stage changes, giving you control over what will be included in the next commit.

**3. Git Directory (Repository)**

Once changes are staged, you commit them to the Git directory using the git commit command. The Git directory stores the metadata and object database for your project. It keeps track of all your commits and the history of your project.

**4. Remote Repository**

When collaborating with others, you push your commits to a remote repository (e.g., GitHub, GitLab). This allows others to access your changes and collaborate on the project. The git push command is used to upload your local commits to the remote repository.

**Example Workflow**

<b>Modify Files:</b> Make changes to your files in the working directory.

<b>Stage Changes:</b> Add changes to the staging area.

```
git add <file_name>
```

<b>Commit Changes:</b> Commit the staged changes to the Git directory.

```
git commit -m "Commit message"
```

<b>Push to Remote:</b> Push your commits to a remote repository.

```
git push origin <branch_name>
```

***Commands Summary***

<body>
<p>Check Status: <b>git status</b></p>
<p>Add to Staging Area: <b>git add <file_name></b></p>
<p>Commit Changes: <b>git commit -m "Commit message"</b></p>
<p>Push to Remote: <b>git push origin <branch_name></b></p>
</body>


<h1>Basic Git Commands</h1>

Initialize a Repository:

```
git init
```

Clone a Repository:

```
git clone <repository_url>
```

Check Status:

```
git status
```
Add Changes to Staging Area:

```
git add <file_name>
```

Commit Changes:
```
git commit -m "Commit message"
```
Push Changes to Remote Repository:
```
git push origin <branch_name>
```
Pull Changes from Remote Repository:

```
git pull origin <branch_name>
```

<h2>Best Practices</h2>

<body>
<p> <h4>Commit Often:</h4> Make small, frequent commits to keep your changes manageable.</p>
<p> <h4>Write Meaningful Commit Messages:</h4> Clearly describe what changes were made and why.</p>
<p> <h4>Use Branches:</h4> Create branches for new features or bug fixes to keep your main branch stable.</p>
<p> <h4>Review Changes:</h4> Use the staging area to review changes before committing them.</p>
</body>
