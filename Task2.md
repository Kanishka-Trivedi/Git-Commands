## Part 1: Git Basics

### Task 1: Install and Configure Git

1. Install git.
2. Configure your git:
```
git config --global user.name "Kanishka Trivedi"
git config --global user.email "kally651997@gmail.com"
```
3. Verify the config list.
```
git config list
```
### Task 2: Initialize a Repository

1. Create a repository and initialize it as a Git Repository to track the changes made in the local repository.
```
mkdir MyProject
cd MyProject
git init
```

## Part 2: Basic Workflow

### Task 3: Creating and Committing Files

1. Create a file:
```
echo "Hi There" > file1.txt
```
NOTE: We use sigle (>) sign to create a new file and (>>) to edit something in the same file.

2. Stage and commit:
```
git add file1.txt
git commit -m "Commit1"
```
### Task 4: Viewing Changes

1. Modify the file:
```
echo "Changes Made" >> file1.txt
```
2. Check file status and differences:
```
git status
git diff
```
### Task 5: Undoing Changes

1. Unstage a staged file:
```
git reset file1.txt
```
2. Discard Uncommited changes:
```
git checkout -- file1.txt
```

## Part 3: Branching and Merging

### Task 6: Branch Management

1. Create a branch and switch to it:
```
git checkout -b branch1
```
2. List branches:
``` 
git branch
```
3. Rename a branch:
```
git branch -m old-branch new-branch
```
### Task 7: Merging Branches

1. Merge ``` new-branch``` to main:
```
git checkout main
git merge new-branch
```
### Task 8: Handling Merge Conflicts

1. Create two conflicting branches and resolve a conflict manually:
```
git merge <branch-name>
```
2. Use:
```
git add <resolved-file>
git commit
```
## Part 4: Remote Repositories

### Task 9: Remote Setup

1. Add a remote repository:
```
git remote add origin repository link
```
2. Verify the remote:
```
git remote -v
```
### Task 10: Push and Pull

1. Push the changes in the repository:
```
git push -u origin main
```
2. Pull changes from the remote:
```
git pull origin main
```
### Task 11: Cloning a Repository

1. Clone the remote repository:
```
git clone repository-link
```

## Part 5: Advanced Git

### Task 12: Stashing Changes

1. Save the uncommited changes using stash:
```
git stash
```
2. Apply stashed changes:
```
git stash apply
```
3. Delete the recent stashed changes:
```
git stash drop
```
### Task 13: Tagging Commits

1. Create and annonate a tag:
```
git tag -a v1.0 -m "Version 1.0 release"
```
2. Push the tags to the remote:
```
git push origin v1.0
```
### Task 14: Rewriting Commit History

1. Use interactive rebase to modify commit messages:
```
git rebase -i HEAD~3
```
### Task 15: Cherry-Picking Commits

1. Apply a specific commit to another branch:
```
git cherry-pick <commit-message>
```

## Part 6: Collaboration

### Task 16: Forking and Pull Requests

1. Fork the repository and clone it locally:
```
git clone repository-link
```
2. Make changes and push them:
```
git checkout -b fix-typo
echo "Typo Fixed" >> README.md
git commit -m "Fixed a typo"
git push origin fix-typo
```
3. Open a pull request on github.

## Part 7: Ignoring Files

### Task 18: Using .gitignore

1. Create a ```.gitignore``` file:
```
echo "node_modules/" > .gitignore
git add .gitignore
git commit -m "Added .gitignore"
```
2. Verify that ignored files are not staged:
```
git status
```
## Part 8: Automation and Cleanup

### Task 19: Cleaning the Repository

1. Remove untracked files:
```
git clean -f
```
### Task 20: Aliases and Shortcuts:
1. Create alias for frequently used commands:
```
git config --global alias.st status
git config --global alias.cm commit
```
2. Use the alias:
```
git st
git cm -m "My personalized commit message"
```
