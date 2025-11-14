# Git Command Guide

A complete categorized reference for Git — from creating a repo and uploading a project to branching, merging, undoing, and managing remotes.

---

## 1. Basics — Create a Repo & Upload a Project

`git init`  
Initialize a new Git repository.

`ls -la`  
Verify the `.git` directory was created.

`git add -A`  
Stage all files for commit (new, modified, deleted).

`git commit -m "Initial commit"`  
Create your first commit with a message.

`git branch -M main`  
Rename the current branch to `main`.

`git remote add origin <repo_url>`  
Connect the local repository to a remote GitHub repository.

`git remote -v`  
View the connected remote repositories.

`git push -u origin main`  
Push commits to the `main` branch and set it as the upstream.

`git pull`  
Fetch and merge changes from the remote repository.

---

## 2. Staging, Committing & Tracking

`git add .`  
Stage all modified or new files in the current directory.

`git add <file>`  
Stage a specific file for commit.

`git restore --staged <file>`  
Unstage a file while keeping changes in your working directory.

`git status`  
Show the current state of the working directory and staging area.

`git commit -m "message"`  
Commit staged changes with a descriptive message.

`git commit --amend`  
Modify or add to the most recent commit.

`git commit -am "message"`  
Stage and commit tracked files in one command.

---

## 3. Viewing History & Changes

`git log`  
Display the complete commit history.

`git log --oneline`  
Show commits in a compact one-line format.

`git log --oneline --graph --decorate --all`  
Visualize all branches and merges in a compact graph.

`git diff`  
Show unstaged changes between working directory and last commit.

`git diff --staged`  
Show changes that have been staged and are ready to commit.

`git show <commit_hash>`  
Display details of a specific commit.

---

## 4. Branching & Merging

`git branch`  
List all branches in the repository.

`git branch <name>`  
Create a new branch.

`git switch <name>`  
Switch to an existing branch.

`git switch -c <name>`  
Create and switch to a new branch.

`git merge <branch>`  
Merge a specified branch into the current branch.

`git branch -d <branch>`  
Delete a merged branch.

`git branch -D <branch>`  
Force delete a branch that hasn’t been merged.

---

## 5. Remote Repositories

`git remote add origin <url>`  
Add a remote repository to your local project.

`git remote -v`  
View all remote repository connections.

`git remote remove origin`  
Remove a remote repository connection.

`git fetch`  
Download commits and branches from a remote repository without merging.

`git pull`  
Fetch and merge changes from the remote repository into the current branch.

`git push origin <branch>`  
Push a specific branch to the remote repository.

`git push --all`  
Push all local branches to the remote repository.

`git push origin --delete <branch>`  
Delete a branch from the remote repository.

`git push -u origin <branch>`  
Push and set an upstream tracking branch.

---

## 6. Undoing / Fixing Mistakes

`git restore --staged <file>`  
Unstage a file that was added accidentally.

`git restore <file>`  
Discard unstaged changes in a file.

`git restore .`  
Discard all unstaged local changes.

`git reset --soft HEAD~1`  
Undo the last commit but keep changes staged.

`git reset --mixed HEAD~1`  
Undo the last commit and unstage the changes.

`git reset --hard HEAD~1`  
Undo the last commit and discard all changes completely.

`git revert <commit_hash>`  
Create a new commit that reverses the effects of a specific commit (safe undo).

---

## 7. Renaming, Deleting, Moving Files

`git rm <file>`  
Delete a tracked file and stage the removal.

`git rm -r <dir>`  
Delete a tracked directory and stage the removal.

`git rm --cached <file>`  
Stop tracking a file but keep it locally.

`git mv <old> <new>`  
Rename or move a file and stage the change.

---

## 8. Ignoring Files

`.gitignore`  
Tells Git which files or directories to ignore.

`node_modules/`  
Ignore Node.js dependencies.

`dist/`  
Ignore build output folders.

`.env`  
Ignore environment variable files.

`*.log`  
Ignore log files.

`.DS_Store`  
Ignore macOS system files.

`git config --global core.excludesfile ~/.gitignore_global`  
Set a global `.gitignore` file for all repositories.

---

## 9. Stashing (Temporary Save)

`git stash`  
Temporarily save uncommitted changes to a stack.

`git stash list`  
List all stashed changes.

`git stash pop`  
Apply the most recent stash and remove it from the stash list.

`git stash apply`  
Apply a stash without removing it from the stash list.

`git stash drop`  
Remove a specific stash entry.

`git stash clear`  
Remove all stashed changes.

---

## 10. Advanced & Inspection

`git ls-files`  
List all tracked files in the repository.

`git config --list`  
Show all current Git configuration settings.

`git config user.name "Name"`  
Set a username for the current repository.

`git config user.email "Email"`  
Set an email for the current repository.

`git config --global user.name "Name"`  
Set your global Git username (for all repos).

`git cat-file -p <hash>`  
Inspect the contents of a Git object (commit/tree/blob).

---

## 11. Cleaning

`git clean -n`  
Preview which untracked files will be deleted (dry run).

`git clean -f`  
Delete untracked files.

`git clean -fd`  
Delete untracked files and directories.

---

## 12. Minimum Commands to Upload Any Project

`cd project-folder`  
Navigate to your project directory.

`git init`  
Initialize a new local Git repository.

`git add -A`  
Stage all files for the first commit.

`git commit -m "Initial commit"`  
Commit all staged files.

`git branch -M main`  
Rename the default branch to `main`.

`git remote add origin https://github.com/username/repo.git`  
Connect the local repo to a GitHub repository.

`git push -u origin main`  
Push your local code to GitHub and set upstream tracking.

---

## Pro Tips

`git status`  
Check repository status frequently to stay updated on changes.

`git log --oneline --graph`  
Visualize branch history in a compact view.

`git revert`  
Use this instead of `git reset --hard` when undoing changes in shared repos.

`git commit`  
Commit small, meaningful changes regularly.

`.gitignore`  
Always add one before your first commit to avoid tracking unwanted files.

---

⭐ **Save this guide** — it’s your quick reference to every Git command you’ll ever need.

