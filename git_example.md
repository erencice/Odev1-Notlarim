# Git Example Scenario

## 🎯 Scenario: Creating a Project and Using Git

### 1️⃣ Initialize a Git Repository
```sh
mkdir my_project          # Create a new project folder
cd my_project            # Enter the project folder
git init                 # Initialize a new Git repository
```

### 2️⃣ Configure Git (Only if not configured before)
```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 3️⃣ Create a File and Track Changes
```sh
touch index.html         # Create an HTML file
echo "<h1>Hello Git</h1>" > index.html  # Add content
git status              # Check status
git add index.html      # Stage the file
git commit -m "Initial commit with index.html"  # Commit changes
```

### 4️⃣ Create and Switch to a New Branch
```sh
git branch feature-1    # Create a new branch
git switch feature-1    # Switch to the new branch
echo "<p>New feature</p>" >> index.html  # Modify file
git add index.html      # Stage changes
git commit -m "Add new feature to index.html"  # Commit changes
```

### 5️⃣ Merge Branch into Main Branch
```sh
git switch master       # Switch back to master
git merge feature-1    # Merge feature-1 into master
git branch -d feature-1 # Delete the feature branch
```

### 6️⃣ Working with Remote Repositories
```sh
git remote add origin https://github.com/user/my_project.git  # Add remote repo
git push -u origin master   # Push changes to remote repo
```

### 7️⃣ Stashing Uncommitted Work
```sh
echo "Temporary change" >> index.html  # Modify file
git stash             # Stash uncommitted changes
git stash list        # View stashed changes
git stash apply       # Reapply last stashed changes
git stash pop         # Apply and remove last stash
git stash clear       # Remove all stashes
```

### 8️⃣ Resetting and Reverting Changes
```sh
git reset HEAD~1       # Undo last commit but keep changes
git reset --hard HEAD~1 # Undo last commit and discard changes
git revert HEAD        # Create a new commit that undoes last commit
```

### 9️⃣ Fetching and Pulling Changes
```sh
git fetch origin       # Fetch latest changes without merging
git pull origin master # Fetch and merge latest changes
```

### 🔟 Cloning and Forking
```sh
git clone https://github.com/user/repo.git  # Clone a repository
# Forking is done on GitHub UI before cloning
```

This scenario provides a hands-on example of how to work with Git effectively! 🚀

