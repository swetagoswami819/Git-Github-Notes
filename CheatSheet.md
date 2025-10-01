# ⚡ Git & GitHub Cheat Sheet

A quick reference for daily Git commands   

---

##  Setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list

# Starting a Project
bash
Copy code
git init               # Initialize a new repo
git clone <url>        # Clone an existing repo

# Basic Commands
bash
Copy code
git status             # Check status
git add <file>         # Stage a file
git add .              # Stage all files
git commit -m "msg"    # Commit changes
git log                # View commit history

# Branching
bash
Copy code
git branch             # List branches
git branch <name>      # Create branch
git checkout <name>    # Switch branch
git checkout -b <name> # Create + switch
git merge <name>       # Merge branch into current

# Remote Repositories
bash
Copy code
git remote -v                       # Show remotes
git remote add origin <url>         # Add remote
git push -u origin main             # Push main branch
git pull origin main                # Pull changes
git fetch                           # Fetch from remote

# Undo & Fix
bash
Copy code
git reset <file>           # Unstage file
git checkout -- <file>     # Discard local changes
git reset --hard HEAD      # Reset to last commit
git revert <commit_id>     # Undo commit safely

# GitHub Workflow
- Fork a repo
- Clone it locally
- Create a new branch
- Commit & Push changes
- Open a Pull Request 

# Shortcuts
bash
Copy code
git log --oneline --graph --all
git diff
git stash
git stash pop

#  Pro Tips
- Always git pull before starting new work
- Write meaningful commit messages
- Use branches for new features
- Keep your main branch clean
