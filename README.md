# Learn Git Easily

## What is Git?
Git is a powerful version control system that helps you track changes in your code and collaborate with others.

# Prerequisites
Let us first creat an new repository in GitHub and we will go from there. Go to  GitHub (https://github.com/) and SignUp/SignIn.

- Click on Repositories and create a new repository named "learn-git-easily". 
Now based on your username in the GitHub Account, you will get the repository link as https://github.com/{username}/learn-git-easily
- For me, my username is "learnsmartcoding" so my repository link is "https://github.com/learnsmartcoding/learn-git-easily"

## Let's go with real time examples
Here's a step-by-step guide to help you get started with the repository "https://github.com/learnsmartcoding/learn-git-easily"


To set your name and email for Git on your local machine, you can use the following commands. Open your terminal or command prompt and type:

Set Your Name: `git config --global user.name "Your Name"`

Replace "Your Name" with your actual name. This command sets your name globally for all Git repositories on your machine.

Set Your Email: `git config --global user.email "your.email@example.com"`

Replace "your.email@example.com" with your actual email address. Similar to the name configuration, this sets your email globally.

By using the --global flag, you are configuring Git to use these settings across all of your Git repositories on your local machine. If you want to set a specific name and email for a particular repository, you can navigate to that repository and omit the --global flag.

To check your Git configuration, you can use:

```
git config --global --get user.name
git config --global --get user.email
```

This will display the configured name and email, allowing you to confirm that your settings have been applied correctly.

# Step 1: Clone the Repository
First, you need to clone the repository to your local machine. Open your terminal or Git Bash and run the following command:

`git clone https://github.com/learnsmartcoding/learn-git-easily.git`

This command will create a local copy of the repository on your machine

# Step 2: Navigate to the Repository
Navigate to the cloned repository using the cd command:

`cd learn-git-easily`

# Step 3: Check the Repository Status
Use the following command to check the status of your local repository:

`git status`

This will show you the current state of your working directory, indicating any changes you've made.

# Step 4: Create a Branch
Before making changes, it's a good practice to create a new branch. This helps to isolate your changes from the main branch. Use the following command to create a new branch:
`git checkout -b your-feature-branch`

Replace "your-feature-branch" with a meaningful name for your branch. E.g. feature/JIRA_ID or feature/add_user

# Step 5: Make Changes
Now, you can make changes to the code using your preferred code editor.

# Step 6: Stage and Commit Changes
Once you've made changes, stage them for commit:

`git add .`

This command stages all changes. If you want to stage specific files, replace `.` with the file names.

Now, commit the changes:

`git commit -m "Your commit message here"`

Replace "Your commit message here" with a concise and descriptive message.

# Step 7: Push Changes to the Remote Repository
Push your changes to the remote repository:

`git push origin your-feature-branch`

e.g. `git push origin feature/JIRA_ID` or `git push origin feature/add_user`

# Step 8: Create a Pull Request
If you're working in a team, create a pull request on the GitHub repository. This allows others to review your changes before merging them into the main branch.

# Step 9: Update Your Local Repository
Periodically, you should update your local repository with changes from the remote repository. Use the following commands:


```
git checkout main
git pull origin main
```


# Additional Commands:
To switch between branches: `git checkout branch-name`
To see a list of branches: `git branch`
To merge branches: `git merge branch-name`
To discard changes in your working directory: `git checkout -- file-name`

These are basic commands to get you started. Git has many more features, so feel free to explore the documentation and learn more as you become more comfortable with the basics.


## In day-to-day Git workflows, you may encounter various scenarios, and different commands are used to handle them. Here are some additional Git commands that are commonly used:

## Pull Changes from Remote:
If your team has made changes to the remote repository, you should pull those changes to your local repository.

`git pull origin main`

This command fetches changes from the remote repository and merges them into your current branch.

## Viewing Commit History:
To see a log of commits, use:

`git log`

You can use `git log --oneline` for a more condensed view.

## See the Differences:
To see the changes between your working directory and the last commit, use:

`git diff`

To see changes in a specific file:
`git diff file-name`

## Discard Local Changes:
To discard changes in a particular file and revert it to the state in the last commit, use: `git checkout -- file-name`

This will replace the changes in file-name with the version from the last commit.

To discard all changes in your working directory and revert all files to the last commit, you can use:

`git reset --hard`

Be cautious with this command as it permanently discards changes.

## Stash Changes:
If you need to switch branches but have uncommitted changes, you can stash them:

Naming Stashes:
When using git stash, you can give a custom name to the stash for better identification. For example:

`git stash save "Your stash message"`

Applying a Specific Stash:
If you have multiple stashes and want to apply a specific one, you can list your stashes:
`git stash list`

It will display a list of stashes with a unique identifier (stash@{0}, stash@{1}, etc.). To apply a specific stash, use:

`git stash apply stash@{n}` 

Replace `n` with the index of the stash you want to apply.

## Deleting Branches:

Local Branch Deletion:
When you delete a branch locally using `git branch -d branch-name`, it only deletes the branch on your local machine

Remote Branch Deletion:
If you want to delete a remote branch, you need to use:

`git push origin --delete branch-to-delete`


## Resolve Merge Conflicts:
If there are merge conflicts during a git pull or git merge, Git will mark the conflicted files. You can use a tool or manually resolve conflicts and then:

```
git add file-name
git merge --continue
```

## Tagging:
Tagging is used to capture a point in history. To create a lightweight tag: `git tag tag-name`

To create an annotated tag with a message: `git tag -a tag-name -m "Tag message"`

To push tags to the remote repository: `git push origin --tags`

# To initialize a Git repository in an existing directory and push the changes to a remote server for the first time, you can follow these steps:

1. Navigate to the Directory:
Open your terminal or command prompt and navigate to the directory where your existing project is located.

`cd path/to/your/directory`

2. Initialize a Git Repository:
Use the following command to initialize a Git repository in the current directory:

`git init`

This command sets up a new Git repository and adds a hidden subfolder within your existing directory that houses the internal data structure required for version control.

3. Add Files to the Staging Area:
Use the git add command to add your existing files to the staging area. This prepares them for the first commit.

`git add .` or `git add --all`

This adds all files in the current directory to the staging area. If you want to add specific files, replace . with the filenames.

4. Commit Changes:
Commit the changes in the staging area to create the initial commit:

`git commit -m "Initial commit"`

Replace "Initial commit" with a meaningful commit message.

5. Create a Remote Repository:
Create a repository on a Git hosting service (e.g., GitHub, GitLab, Bitbucket). Follow the instructions on the platform to create a new repository.

6. Add Remote Repository URL:
Add the remote repository URL to your local repository. Replace <remote-url> with the URL of your remote repository.

`git remote add origin <remote-url>`

7. Push Changes to the Remote Repository:
Push your local changes to the remote repository. The -u option sets up tracking, so you can simply use git push in the future.

`git push -u origin master`

Replace "master" with the branch name you want to push.

That's it! Your existing directory and its content are now part of a Git repository, and the changes have been pushed to the remote server for the first time.

# Git has its own terminology that helps describe the various components and processes involved in version control. Here are some key Git terminologies explained

## Repository (Repo)
Local Repository: This is the copy of the Git repository that resides on your local machine. You interact with this repository while making changes, committing, and branching. Use git init to initialize a new local repository.

## Remote Repository (Server Repository): 
This is a repository hosted on a remote server (like GitHub, GitLab, Bitbucket). You can push your changes to and pull changes from this repository. Use git remote add to connect your local repository to a remote repository.

## Working Directory
The working directory is the directory on your local machine where you are actively making changes to your files.

## Staging Area (Index)
The staging area is a space where you can list and review changes before committing them. Files in the staging area are part of the next commit. You use git add to move changes from the working directory to the staging area.

## Commit
A commit is a snapshot of your changes at a particular point in time. Each commit has a unique identifier (SHA-1 hash) and includes information about the changes made, the author, and a commit message. Use git commit to create a commit.

## Branch
A branch is an independent line of development in Git. You can create branches to work on new features or bug fixes without affecting the main codebase. Use git branch to see existing branches and git checkout or git switch to switch between branches.

## Merge
Merging combines changes from different branches into a single branch. Use git merge to merge changes.

## Pull Request (PR)
A pull request is a way to propose changes to a codebase in a collaborative manner. It's commonly used in platforms like GitHub and GitLab. It allows others to review and discuss your changes before merging them into the main branch.

## Push
Pushing refers to uploading your local changes to a remote repository. Use git push to send your commits to the server.

## Pull
Pulling refers to fetching changes from a remote repository and merging them into your local branch. Use git pull to update your local repository with changes from the remote repository.

## Clone
Cloning is the process of creating a copy of a remote repository on your local machine. Use git clone followed by the repository URL.

## Stash
Stashing allows you to temporarily save changes that are not ready to be committed. Use git stash to stash changes and git stash apply to reapply them.

These are some of the fundamental terms in Git. Understanding these concepts is crucial for effective version control and collaboration in a software development project.