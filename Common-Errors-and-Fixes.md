# ❌ Common Git & GitHub Errors & Fixes

A quick list of common problems I faced while using Git & GitHub, and how to solve them  

```bash
## 1. fatal: not a git repository
Cause: You’re running Git commands in a folder that’s not initialized as a repo.
Fix:
git init
or go to the correct folder that has .git/.

## 2. fatal: remote origin already exists
Cause: You already added a remote with the same name.
Fix:
git remote remove origin
git remote add origin <url>


## 3. Updates were rejected because the remote contains work…
Cause: Remote has changes you don’t have locally.
Fix:
git pull origin main --rebase
git push origin main

## 4. Merge Conflicts
Cause: Two people edited the same lines.
Fix:
Open the file, look for <<<<<<<, =======, >>>>>>>
Edit manually to keep the right changes
Stage & commit again.

## 5. fatal: could not read Username for 'https://github.com'
Cause: GitHub authentication issue.
Fix:
Use SSH keys or
Run:
git config --global credential.helper store
and login again.

6. Detached HEAD state
Cause: You checked out a specific commit, not a branch.
Fix:
git checkout main
or create a new branch:
git checkout -b new-branch

## 7. fatal: pathspec 'branch-name' did not match
Cause: The branch name doesn’t exist.
Fix: Check existing branches:
git branch -a

## 8. Permission denied (publickey)
Cause: SSH key not set up with GitHub.
Fix:
Generate a key: ssh-keygen -t rsa -b 4096
Add the public key to GitHub → Settings → SSH & GPG keys.

## 9. error: failed to push some refs
Cause: Branch not tracking remote branch.
Fix:
git push -u origin branch-name


## Pro Tip
If you’re ever stuck, run:
- git status
- It almost always tells you what’s wrong 😉

