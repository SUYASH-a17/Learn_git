# Learn_git
learning Git

**Git init** - Initializes an empty repo by creating .git file  
**rm -rf .git** - removes the .git file and deletes the entire working history  
**ls -la** - shows the list of files in the repo  
**git add -A** - Stages all changes in the repository, regardless of their status (new, modified, or deleted)  
**git commit -m 'First Commit'** - Did a first commit  
**git log** - get the log of all the commits  
**git status** - shows the current state of the working directory and staging area, to understand what changes have been made and which are ready to be committed.
**git restore --staged [file_name]** - restore the file before committing to the previous stage.
**git restore** . - restore the changes
**gitignore** - store text/data which won't be tracked by git
**global ignore file- git config --global core.excludesfile [file]
**git rm -r --cached [file/folder/.]** - clear the cache
**git rm home.html** - deletes the file and moves to staging(does the git add . command) for us so we are ready to commit
**git mv home.html index.html** - rename a file
**git diff** - shows the difference between 2 commit
**git log --oneline** - shows logs in oneline with a hash number
**git commit --amend** - modifies/make changes to a commit
**git reset** [hash#] - reset the commit msg
**git reset --hard** [hash#] - rewind back to a specific commit history and go forward from there as it deletes all the files after the hash#
Commands:
 p, pick <commit> = use commit
 r, reword <commit> = use commit, but edit the commit message
 e, edit <commit> = use commit, but stop for amending
 s, squash <commit> = use commit, but meld into previous commit
 f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
                    commit's log message, unless -C is used, in which case
                    keep only this commit's message; -c is same as -C but
                    opens the editor
 x, exec <command> = run command (the rest of the line) using shell
 b, break = stop here (continue rebase later with 'git rebase --continue')
 d, drop <commit> = remove commit
 l, label <label> = label current HEAD with a name
 t, reset <label> = reset HEAD to a label
 m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
         create a merge commit using the original merge commit's
         message (or the oneline, if no original merge commit was
         specified); use -c <commit> to reword the commit message
 u, update-ref <ref> = track a placeholder for the <ref> to be updated
                       to this position in the new commits. The <ref> is
                       updated at the end of the rebase
*GIT FLOW*
    git switch -c ['branch_name'] - create a new branch and make the required changes in it 
    git merge ['branch_name'] - merge the new branch with the current/main branch
    git branch -d ['branch_name'] - delete the new branch after making changes

**git merge --abort** -  abort the merge
**git stash** - Temporarily saves changes in your working directory without committing them, allowing you to switch branches or work on something else.
**git clean** - Removes untracked files and directories from your working directory.
