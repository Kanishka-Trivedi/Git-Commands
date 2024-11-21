## Part 1: Understanding and Using git stash

### Task 1: Save Changes Temporarily with git stash

1. Make changes to a file without committing:
```
echo "Temporary changes" >> temp-file.txt
```
2. View the status of changes:
```
git status
```
3. Stash the changes: This command saves changes to a stash and restores the working directory to the last commit state.
```
git stash
```
4. View the stashed changes:
```
git stash list
```

## Part 4: Cherry-Picking Commits (git cherry-pick)
### Task 8: Pick a Specific Commit
1. View the commit history to find the commit hash you want to cherry-pick: This will show us all the commit hash codes list.
```
git log --oneline
```
2. Cherry-pick a specific commit by its hash:
```
git cherry-pick <commit-hash>
```
3. Resolve conflicts if any, then commit the changes:
```
git add .
git cherry-pick --continue
```
## Part 6: Working with Remote Repositories

### Task 12: Add a Remote Repository

1. Add a remote repository URL to the project:
```
git remote add origin repository-link
```
### Task 13: Fetch Changes from Remote

1. Fetch changes from the remote repository without merging them:
```
git fetch origin
```
2. View fetched branches:
```
git branch -r
```
### Task 14: Pull Changes from Remote

1. Pull the latest changes from the remote repository and merge them into the local branch:
```
git pull origin main
```
### Task 15: Push Changes to Remote

1. Push local changes to the remote repository:
```
git push origin main
```
2. Push a new branch to the remote repository:
```
git push origin new-branch
```
### Task 16: Delete Remote Branch

1. Delete a remote branch:
```
git push origin --delete new-branch
```

## Part 7: Forking and Contributing to Open-Source Projects

### Task 17: Fork a Repository on GitHub
1. Go to the desired github repository and click the green button of fork option to create the copy of that repository.
2. Clone the forked repository:
```
git clone repository-link
```
### Task 18: Make Changes and Commit
1. Create a new branch for your changes:
```
git checkout -b branchA
```
2. Make changes to the code (e.g., fix a typo in README.md), stage, and commit them:
```
git add README.md
git commit -m "practice"
```

### Task 19: Push Changes to Your Fork
1. Push the changes to your remote fork:
```
git push origin branchA
```
### Task 20: Create a Pull Request
1. Go to the forked repository and click on compare and pull request.
2. Write the discription and give a title and then create a new pull request.

### Task 21: Sync Your Fork with the Original Repository
1. 