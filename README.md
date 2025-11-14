# 🧩 Git Command Guide

A complete categorized reference for Git — from creating a repo and uploading a project to branching, merging, undoing, and managing remotes.

---

## 🧱 1. Basics — Create a Repo & Upload a Project

`
git init                      # Initialize a new Git repository  
ls -la                        # Verify .git directory  
git add -A                    # Stage all files  
git commit -m "Initial commit" # Save a snapshot  
git branch -M main            # Rename current branch to main  
git remote add origin <repo_url>  # Connect to remote (GitHub)  
git remote -v                 # Verify remote  
git push -u origin main       # Push commits to GitHub  
git pull                      # Fetch + merge remote changes  
`

---

## 🗂️ 2. Staging, Committing & Tracking

`
git add .                     # Stage modified/new files  
git add <file>                # Stage specific file  
git restore --staged <file>   # Unstage a file  
git status                    # Check working directory status  
git commit -m "message"       # Commit staged files  
git commit --amend            # Modify last commit  
git commit -am "message"      # Skip staging (for tracked files)  
`

---

## 🔍 3. Viewing History & Changes

`
git log                       # Show full commit history  
git log --oneline             # One-line summary of commits  
git log --oneline --graph --decorate --all  # Visualize branches  
git diff                      # Show unstaged changes  
git diff --staged             # Show staged changes  
git show <commit_hash>        # Show specific commit details  
`

---

## 🌿 4. Branching & Merging

`
git branch                    # List branches  
git branch <name>             # Create new branch  
git switch <name>             # Switch to branch (modern)  
git switch -c <name>          # Create + switch  
git merge <branch>            # Merge branch into current  
git branch -d <branch>        # Delete merged branch  
git branch -D <branch>        # Force delete branch  
`

---

## 🌐 5. Remote Repositories

`
git remote add origin <url>   # Add remote repo  
git remote -v                 # View remotes  
git remote remove origin      # Remove remote  
git fetch                     # Download objects and refs  
git pull                      # Fetch + merge  
git push origin <branch>      # Push a specific branch  
git push --all                # Push all branches  
git push origin --delete <branch>  # Delete remote branch  
git push -u origin <branch>   # Set upstream tracking  
`

---

## ♻️ 6. Undoing / Fixing Mistakes

`
git restore --staged <file>   # Unstage file  
git restore <file>            # Discard unstaged changes  
git restore .                 # Discard all local changes  
git reset --soft HEAD~1       # Undo last commit (keep staged)  
git reset --mixed HEAD~1      # Undo last commit (keep changes unstaged)  
git reset --hard HEAD~1       # Undo last commit (discard all changes)  
git revert <commit_hash>      # Create new commit that undoes old one  
`

---

## 📁 7. Renaming, Deleting, Moving Files

`
git rm <file>                 # Delete tracked file  
git rm -r <dir>               # Delete tracked directory  
git rm --cached <file>        # Stop tracking (keep local)  
git mv <old> <new>            # Rename/move file  
`

---

## 🚫 8. Ignoring Files

`
# .gitignore file  
node_modules/  
dist/  
.env  
*.log  
.DS_Store  

# Global ignore  
git config --global core.excludesfile ~/.gitignore_global  
`

---

## 💾 9. Stashing (Temporary Save)

`
git stash                     # Save uncommitted changes  
git stash list                # View all stashes  
git stash pop                 # Apply & remove last stash  
git stash apply               # Apply without removing  
git stash drop                # Delete a stash  
git stash clear               # Clear all stashes  
`

---

## 🧠 10. Advanced & Inspection

`
git ls-files                  # Show tracked files  
git config --list             # View Git config  
git config user.name "Name"   # Set local username  
git config user.email "Email" # Set local email  
git config --global user.name "Name"  # Set global username  
git cat-file -p <hash>        # Inspect commit/blob/tree  
`

---

## 🧹 11. Cleaning

`
git clean -n                  # Preview untracked files  
git clean -f                  # Remove untracked files  
git clean -fd                 # Remove untracked files + folders  
`

---

## 🏁 12. Minimum Commands to Upload Any Project

`
cd project-folder  
git init  
git add -A  
git commit -m "Initial commit"  
git branch -M main  
git remote add origin https://github.com/username/repo.git  
git push -u origin main  
`

---

## 🧾 Pro Tips

- Use `git status` and `git log --oneline --graph` often.  
- Prefer `git revert` over `git reset --hard` for public repos.  
- Commit frequently with meaningful messages.  
- Add `.gitignore` before the first commit to avoid tracking unwanted files.  

---

⭐ **Save this guide** — it’s your quick reference to every Git command you’ll ever need.
