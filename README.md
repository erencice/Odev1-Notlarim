# Basic Terminal Commands & Git Essentials

## 📌 Terminal Commands

### 📂 Directory & File Management
```sh
pwd                     # Print working directory
ls                      # List directory contents
cd                      # Change directory
clear                   # Clear terminal screen

mkdir FolderName        # Create a new directory
rm -rf FolderName       # Remove directory and its contents

touch FileName.ext      # Create an empty file
rm FileName.ext         # Delete a file
```

---

## 🚀 Git Configuration

### 🔧 Setting Global Configurations
```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Change default editor
git config --global core.editor "/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl --new-window --wait"
```

---

## 🔍 Understanding Git Basics

### 📌 Staging Area
Git introduces a unique concept called the **staging area (index)**, which acts as an intermediate step before committing changes. This allows you to:
- Stage selected files before committing.
- Commit only relevant changes without affecting unrelated modifications.
- Selectively stage portions of a file for better commit granularity.

💡 **Tip:** If you want to bypass the staging area and commit all changes at once, use `git commit -a`.

### 📁 Git Repository
A Git repository is stored in the `.git/` folder of your project. It tracks changes and maintains the entire history of your project. **Deleting the `.git/` folder erases all version history!**

---

## ⚡ Git Commands

### 🛠️ Repository Initialization & Status
```sh
git status             # Check the status of the working directory
git init               # Initialize a new Git repository (Run only if needed)
ls -la                 # List all files including hidden ones
```

### 📌 Staging & Committing Changes
```sh
git add .              # Stage all changes
git add FileName.ext   # Stage specific file
git commit -m "Commit message"  # Commit staged changes with a message
git log                # View commit history
```

### 🛑 Excluding Files with .gitignore
```sh
touch .gitignore       # Create .gitignore file to exclude specific files
# Use GitHub's gitignore templates for various programming languages
```

### 🔀 Branching & Merging
```sh
git branch NewBranch   # Create a new branch
git switch NewBranch   # Switch to the new branch
git switch master      # Switch to master branch
git merge NewBranch    # Merge a branch into the current branch
```

When you run `git switch` or `git branch`, any commits you make afterward will apply to that specific branch. This allows you to work on isolated features without affecting the main codebase.

### 🔄 Fast Forwarding
Fast forwarding occurs when Git can simply move your branch pointer forward because there is a linear path from the current branch to the target branch. This happens when the current branch hasn't diverged from the branch being merged.

### 🚧 Handling Merge Conflicts
```sh
git status             # Identify conflicted files
# Edit the conflicted files and resolve conflicts
git add <resolved-file>  # Mark as resolved
git commit              # Complete the merge
```
To cancel a conflicted merge:
```sh
git merge --abort       # Cancel the merge operation
```

---

## 🎭 Stashing Changes
### 📌 Saving Work Without Committing
```sh
git stash              # Save current changes and revert to the last commit
```

### 📌 Applying Stashed Changes
```sh
git stash pop          # Apply and remove the last stashed change
git stash apply        # Apply the last stashed change but keep it in stash
```

### 📌 Managing Stashes
```sh
git stash list         # List all stashes
git stash clear        # Remove all stashes
```

---

## 🏗️ Resetting & Reverting Changes

### 📌 Undoing Changes
```sh
git checkout <commit-hash>    # Temporarily switch to an older commit
git checkout -- <file>        # Discard changes in a specific file
```

### 📌 Resetting Commits
```sh
git reset <commit-hash>       # Move HEAD to a previous commit (keeps changes)
git reset --hard <commit-hash> # Move HEAD and delete all changes permanently
```

### 📌 Reverting Commits
```sh
git revert <commit-hash>      # Undo a commit by creating a new commit
```

---

## 🔍 Comparing & Rebasing

### 📌 Viewing Differences
```sh
git diff                     # Show unstaged changes
git diff --staged            # Show staged changes
```

### 📌 Rebasing
Rebasing rewrites commit history, integrating changes in a linear fashion.
```sh
git rebase branch_name       # Apply changes from another branch linearly
```

---

## 🚀 Pushing & Pulling Changes

### 📌 Pushing Changes to Remote
```sh
git push origin branch_name  # Push changes to the remote repository
```

### 📌 Pulling Changes
```sh
git pull origin branch_name  # Fetch and merge changes from remote
```

### 📌 Fetch vs. Pull
```sh
git fetch                    # Retrieve changes but don’t merge
git pull                      # Fetch and merge updates
```

---

## 🌎 Working with Remote Repositories

### 📌 Cloning a Repository
```sh
git clone <repo_url>         # Clone a remote repository locally
```

### 📌 Forking a Repository
Forking creates a personal copy of a repository under your GitHub account, allowing you to contribute without affecting the original project.

### 📌 Creating a Pull Request
A **pull request** is a way to propose changes to a remote repository and get them reviewed before merging.

### 🔒 Private Repositories
Private repositories restrict access, ensuring that only authorized users can view and contribute.

---

💡 **Mastering these commands will significantly enhance your workflow and productivity with Git & the terminal!** 🚀
