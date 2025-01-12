# Git & GitHub Cheatsheet

## General Commands
- **Initialize Repository:** `git init`
- **Check Repository Status:** `git status`
- **View Help:** `git help command`

## Configuration
- **Configure User Details:**
  - Set name: `git config --global user.name "Your Name"`
  - Set email: `git config --global user.email "your_email@example.com"`
- **View Configuration:** `git config --list`
- **Edit Configuration:** `git config --global --edit`

## Staging and Unstaging
- **Stage Files:**
  - Specific file: `git add filename`
  - All files: `git add .`
- **Stage Portions of a File:** `git add -p`
- **Unstage File:** `git reset filename`

## Committing Changes
- **Commit Changes:**
  - Commit with message: `git commit -m "commit message"`
  - Amend last commit: `git commit --amend`
- **View Commit History:** `git log`
- **Compact Log Format:** `git log --oneline`
- **Log with File Changes:** `git log --stat`
- **Log by Author:** `git log --author="Author Name"`
- **Log for Specific File:** `git log filename`
- **Graphical Log:** `git log --graph --decorate --oneline`

## Working with Branches
- **Create a Branch:**
  - Only create: `git branch branch_name`
  - Create and switch: `git checkout -b branch_name`
- **Rename Current Branch:** `git branch -m new_branch_name`
- **Switch Branch:** `git checkout branch_name`
- **List All Remote Branches:** `git branch -r`
- **Track a Remote Branch Locally:** `git checkout --track origin/branch_name`
- **Delete Branch:**
  - Local branch: `git branch -d branch_name`
  - Remote branch: `git push origin --delete branch_name`
- **Merge Branch:** `git merge branch_name`
- **Rebase Branch:** `git rebase branch_name`
- **Interactive Rebase:** `git rebase -i commit_hash`

## Remote Repositories
- **Push to Remote Repository:** `git push`
- **Pull Changes from Remote:** `git pull`
- **Clone Repository:** `git clone repository_url`
- **Set Remote Repository:** `git remote add origin repository_url`
- **View Remote URLs:** `git remote -v`
- **Fetch Changes:** `git fetch`

## Stashing Changes
- **Stash Changes:**
  - Save changes: `git stash`
  - Apply last stash: `git stash apply`
  - View stash list: `git stash list`

## Viewing Differences
- **View Differences:**
  - Between working directory and index: `git diff`
  - Between commits: `git diff commit1 commit2`

## Tagging
- **Tagging:**
  - Create tag: `git tag tag_name`
  - Push tags: `git push --tags`

## Undoing Changes
- **Undo Changes:**
  - Discard uncommitted changes: `git checkout -- filename`
  - Reset to last commit: `git reset --hard HEAD`
- **Revert Commit:** `git revert commit_hash`

## Advanced Reset
- **Soft Reset:** `git reset --soft HEAD~n` (Keep changes staged, reset last `n` commits)
- **Mixed Reset:** `git reset --mixed HEAD~n` (Unstage changes, keep them in the working directory)
- **Hard Reset:** `git reset --hard HEAD~n` (Remove last `n` commits and discard changes)

## GitHub-Specific Commands
- **Create Pull Request:** `gh pr create`
- **View Issues:** `gh issue list`
- **Fork Repository:** Use the GitHub web interface

## Advanced Commands
- **Squash Commits:** Combine multiple commits into one
  - Start rebase: `git rebase -i HEAD~n` (where `n` is the number of commits)
  - Mark commits to squash and save.
- **Bisect to Find Bugs:**
  - Start bisect: `git bisect start`
  - Mark good commit: `git bisect good commit_hash`
  - Mark bad commit: `git bisect bad commit_hash`
- **Cherry-Pick Commit:** Apply changes from a specific commit
  - `git cherry-pick commit_hash`

## Troubleshooting
- **Resolve Merge Conflicts:**
  - Check conflicts: `git status`
  - Resolve files manually, then stage them: `git add filename`
  - Complete merge: `git commit`
- **Abort a Merge:** `git merge --abort`
- **Abort a Rebase:** `git rebase --abort`

## Viewing Repository Details
- **View Commit Graph:** `git log --graph --oneline --all`
- **Show Changes for a Commit:** `git show commit_hash`
- **List All Branches:** `git branch -a`

## Cleanup
- **Remove Untracked Files:** `git clean -f`
- **Remove Directories:** `git clean -fd`
- **Prune Remote Tracking Branches:** `git remote prune origin`

## Aliases
- Set up shortcuts for frequent commands:
  - Example: `git config --global alias.co checkout`  
  - Then use `git co branch_name` instead of `git checkout branch_name`.

