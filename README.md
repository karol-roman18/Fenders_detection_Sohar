#Defect prediction in Sohar Port using YOLOv8

Tutorial for using git

#Credits for this readme go to Mathijsvb (Mathijs van Binnendijk) who wrote this tutorial

---

## Git Basics Tutorial

I quickly noted down the basics of using git. I'll covers essential Git commands such as cloning, committing, pulling, pushing, and creating and working in your own branch.

### Prerequisites

Before you begin, make sure you have Git installed on your local machine. You can download Git from [git-scm.com](https://git-scm.com/downloads) and follow the installation instructions for your operating system.

### Cloning a Repository

To start working with a Git repository, you typically begin by cloning it to your local machine.

```shell
git clone https://github.com/Mathijsvb/Resin-flow-field-prediction.git
```

### Pulling Changes
To update your local repository with changes made by others, use the git pull command. Don't forget to do this whenever external changes are made!

* `git pull` fetches changes from the remote repository and merges them into your local branch.

Note that pulling only pulls for the specific branch you're on.

### Working in Your Own Branch
It's a good practice to work in your own branch when making changes to avoid conflicts with the main or master branch. Trust me it will save you a lot of headace! Please always push to your branch and then we can later merge that branch with main if needed.

* `git checkout -b your-branch-name` creates a new branch named `your-branch-name` and switches to it.

To push your branch to the remote repository, use the `git push` command with the `-u` flag the first time you push.

* `git push -u origin your-branch-name` sets up a tracking relationship between your local branch and the remote branch on the origin repository.

To switch to an existing branch, use the `git checkout` command.

* `git checkout your-branch-name`

### Committing Changes
After making changes to the files in your local repository, you need to commit those changes to create a new version.

* `git add .` stages all changes in your working directory for the commit. You can choose add only specific files as well.
* `git commit -m "Your commit message here"` commits the changes with a descriptive message. Please do write the commit message!

After commiting the changes we can push them to the remote repository

### Pushing Changes
When you want to share your local changes with others or update the remote repository, use the git push command.

* `git push` sends your committed changes to the remote repository to the branch you've checked out.


> :warning: Avoid pushing directly to the main branch. It's a best practice to work in your own branch, and changes should be merged into the main branch through a pull request. Directly pushing to the main branch can lead to conflicts and disruptions.

### Some useful commands
These were the basics of git! Here is a list of the discussed commands + extras:

```Bash
# Initialize a new Git repository in the current directory
git init

# Git Clone: Cloning a remote repository to your local machine.
git clone [repository_url]

# Show the status of the repository (untracked, modified, etc.)
git status

# Add specific file(s) to the staging area
git add [file]

# Commit changes and open a text editor to write commit messages
git commit

# Commit all changes and open a text editor to write commit messages
git commit -a

# Commit all changes with a message without opening a text editor
git commit -am "Your commit message"

# Temporarily save changes that are not ready for a commit.
git stash

# Show the commit history
git log

# Show a nice commit history with branches and decorations
git log --all --graph --decorate

# Move the HEAD to a specific commit by its hash
git checkout [hash]

# Switch back to the 'main' branch
git checkout main

# Forcefully checkout (discard changes in the working directory)
git checkout -f ...

# Commit n commits back from the current HEAD
git commit HEAD~[n]

# Show the differences between two specific commits
git diff [hash]

# Show differences between HEAD and n commits back
git diff HEAD~[n]

# Show the differences between the working directory and the last commit
git diff

# Create a new branch with the given name
git branch [name]

# List all branches in the repository
git branch

# Create and switch to a new branch
git checkout -b [name]

# Merge changes from another branch into the current branch
git merge [branch]

# Resolve merge conflicts manually in the code editor
# (This typically involves editing conflicted files)
# After resolving conflicts, continue with the merge
git merge --continue

# Add a remote repository named 'origin' (can use a different name)
git remote add origin [site]

# List remote repositories and their URLs
git remote -v

# Fetching changes from a remote repository without automatically merging them.
git fetch

# Pull changes from the remote branch you're tracking
git pull

# Push changes to the remote branch you're tracking
git push

# Read all the data in a specific commit
git cat-file -p [hash]

# Reset the last n commits, keeping changes in the working directory
git reset HEAD~[n]

```
