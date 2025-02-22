# Learning Git

## Basic Commands
- **`git init`**: Initializes an empty repo by creating `.git` file
- **`rm -rf .git`**: Removes the `.git` file and deletes the entire working history
- **`ls -la`**: Shows the list of files in the repo
- **`git add -A`**: Stages all changes in the repository, regardless of their status (new, modified, or deleted)
- **`git commit -m 'First Commit'`**: Makes a first commit
- **`git log`**: Gets the log of all the commits
- **`git status`**: Shows the current state of the working directory and staging area to understand what changes have been made and which are ready to be committed
- **`git restore --staged [file_name]`**: Restores the file before committing to the previous stage
- **`git restore .`**: Restores the changes
- **`.gitignore`**: Stores text/data which won't be tracked by Git
  - **Global ignore file**: `git config --global core.excludesfile [file]`
- **`git rm -r --cached [file/folder/.]`**: Clears the cache
- **`git rm home.html`**: Deletes the file and moves it to staging, making it ready to commit
- **`git mv home.html index.html`**: Renames a file
- **`git diff`**: Shows the difference between two commits
- **`git log --oneline`**: Shows logs in one line with a hash number
- **`git commit --amend`**: Modifies/makes changes to a commit
- **`git reset [hash#]`**: Resets the commit message
- **`git reset --hard [hash#]`**: Rewinds back to a specific commit history and goes forward from there, deleting all the files after the hash#

## Rebase Commands
- **p, pick**: Use commit
- **r, reword**: Use commit, but edit the commit message
- **e, edit**: Use commit, but stop for amending
- **s, squash**: Use commit, but meld into previous commit
- **f, fixup [-C | -c]**: Like "squash" but keeps only the previous commit's log message, unless `-C` is used, in which case keeps only this commit's message; `-c` is the same as `-C` but opens the editor
- **x, exec**: Run command (the rest of the line) using shell
- **b, break**: Stop here (continue rebase later with `git rebase --continue`)
- **d, drop**: Remove commit
- **l, label**: Label current HEAD with a name
- **t, reset**: Reset HEAD to a label
- **m, merge [-C | -c] [# ]**: Create a merge commit using the original merge commit's message (or the one line, if no original merge commit was specified); use `-c` to reword the commit message
- **u, update-ref**: Track a placeholder for the to be updated to this position in the new commits. The is updated at the end of the rebase

## Git Flow Commands
- **`git switch -c ['branch_name']`**: Create a new branch and make the required changes in it
- **`git merge ['branch_name']`**: Merge the new branch with the current/main branch
- **`git branch -d ['branch_name']`**: Delete the new branch after making changes
- **`git merge --abort`**: Abort the merge
- **`git stash`**: Temporarily saves changes in your working directory without committing them, allowing you to switch branches or work on something else
- **`git clean`**: Removes untracked files and directories from your working directory
