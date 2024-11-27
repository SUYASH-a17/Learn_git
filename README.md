# Learn_git
learning Git

Git init - Initializes an empty repo by creating .git file
rm -rf .git - removes the .git file and deletes the entire working history
ls -la - shows the list of files in the repo
git add -A - Stages all changes in the repository, regardless of their status (new, modified, or deleted)
git commit -m 'First Commit' - Did a first commit 
git log - get the log of all the commits
git status - shows the current state of the working directory and staging area, to understand what changes have been made and which are ready to be committed.
git restore --staged [file_name] - restore the file before committing to the previous stage.
git restore . - restore the changes
gitignore - store text/data which won't be tracked by git
global ignore file- git config --global core.excludesfile [file]
git rm -r --cached [file/folder/.]- clear the cache
git rm home.html - deletes the file and moves to staging(does the git add . command) for us so we are ready to commit
git mv home.html index.html - rename a file
git diff - shows the difference between 2 commit
git log --oneline - shows logs in oneline with a hash number
git commit --amend - modifies/make changes to a commit