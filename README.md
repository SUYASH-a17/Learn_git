# -------------------------
# 1. Basics — Create & upload
# -------------------------
git init                      # Initialize a new Git repository (creates .git directory)
ls -la                        # Show files (verify .git created)
git add -A                    # Stage all changes (new, modified, deleted)
git commit -m "Initial commit" # Commit staged changes with a message
git branch -M main            # Rename current branch to 'main'
git remote add origin <repo_url>  # Add remote repo URL (GitHub)
git remote -v                 # Verify remote(s) are set
git push -u origin main       # Push local main to remote and set upstream
git pull                      # Fetch + merge remote changes

# ------------------------------------
# 2. Staging, Committing & Tracking
# ------------------------------------
git add .                     # Stage modified and new files in current dir
git add <file>                # Stage a specific file
git restore --staged <file>   # Unstage a file (keep working-tree changes)
git status                    # Show working tree and staging status
git commit -m "message"       # Commit staged files with message
git commit --amend            # Amend the last commit (message or content)
git commit -am "message"      # Add & commit tracked files (skips staging step for tracked files)

# ------------------------------------
# 3. Viewing history & differences
# ------------------------------------
git log                       # Show full commit history
git log --oneline             # Compact one-line summary of commits
git log --oneline --graph --decorate --all  # Visualize branches & merges
git diff                      # Show unstaged changes (working tree vs index)
git diff --staged             # Show staged changes (index vs HEAD)
git show <commit_hash>        # Show details & diff of a specific commit

# ------------------------------------
# 4. Branching & merging
# ------------------------------------
git branch                    # List local branches
git branch <name>             # Create a new branch
git switch <name>             # Switch to branch (newer, clearer than checkout)
git switch -c <name>          # Create and switch to a new branch
git merge <branch>            # Merge <branch> into current branch
git branch -d <branch>        # Delete branch (safe delete if merged)
git branch -D <branch>        # Force delete branch (even if unmerged)

# ------------------------------------
# 5. Remotes
# ------------------------------------
git remote add origin <url>   # Add a remote named 'origin'
git remote -v                 # Show remotes + URLs
git remote remove origin      # Remove the 'origin' remote
git fetch                     # Download remote refs & objects (no merge)
git pull                      # Fetch + merge (default)
git push origin <branch>      # Push a branch to the remote
git push --all                # Push all branches
git push origin --delete <branch>  # Delete a branch on the remote
git push -u origin <branch>   # Push and set remote tracking for this branch

# ------------------------------------
# 6. Undo / fix mistakes
# ------------------------------------
git restore --staged <file>   # Unstage (remove from index) but keep working changes
git restore <file>            # Discard unstaged working-tree changes for <file>
git restore .                 # Discard all unstaged changes (working tree → index state)
git reset --soft HEAD~1       # Move HEAD back 1 commit; keep changes staged
git reset --mixed HEAD~1      # Move HEAD back 1 commit; keep changes unstaged (default)
git reset --hard HEAD~1       # Move HEAD back 1 commit and discard all changes (destructive)
git revert <commit_hash>      # Create a new commit that reverses <commit_hash> (safe for published history)

# ------------------------------------
# 7. File operations
# ------------------------------------
git rm <file>                 # Remove tracked file and stage deletion
git rm -r <dir>               # Remove tracked directory recursively
git rm --cached <file>        # Stop tracking file but keep it locally
git mv <old> <new>            # Rename/move file and stage the change

# ------------------------------------
# 8. Ignore files
# ------------------------------------
# Add a .gitignore file with entries like:
# node_modules/
# dist/
# .env
# *.log
# .DS_Store
git config --global core.excludesfile ~/.gitignore_global  # Set a global ignore file

# ------------------------------------
# 9. Stashing (temporary save)
# ------------------------------------
git stash                     # Save uncommitted changes to a stack
git stash list                # List stashes
git stash pop                 # Reapply last stash and drop it
git stash apply               # Reapply stash but keep it in the stash list
git stash drop                # Delete a stash entry
git stash clear               # Remove all stashes

# ------------------------------------
# 10. Advanced / inspection
# ------------------------------------
git ls-files                  # List files tracked by Git
git config --list             # Show Git configuration
git config user.name "Name"   # Set repo-local username
git config user.email "a@b"   # Set repo-local email
git config --global user.name "Name"  # Set global username
git cat-file -p <hash>        # Inspect an object (commit/blob/tree)

# ------------------------------------
# 11. Cleaning (destructive!)
# ------------------------------------
git clean -n                  # Show which untracked files would be removed (dry-run)
git clean -f                  # Remove untracked files
git clean -fd                 # Remove untracked files and directories

# ------------------------------------
# 12. Minimum sequence to upload a project
# ------------------------------------
cd project-folder
git init
git add -A
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/repo.git
git push -u origin main
