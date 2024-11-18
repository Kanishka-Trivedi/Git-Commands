## Part 1: Creating and Cloning Repositories
### Task 1: Create a Local Git Repository

1. Task 1: Create a Local Git Repository:
```
mkdir MyProject
cd MyProject
```
2. Initialize the git folder:
```
git init
```
3. Verify the repository status:
```
git status
```
### Task 2: Clone a Remote Repository

1. Clone a GitHub repository:
```
git clone repo-link
```
2. Verify the cloned repository structure:
```
cd repo
ls -a
```

## Part 2: Understanding Commits and Commit Messages

### Task 3: Commit Changes Locally

1. Create a new file and add content:
```
echo "Hello I'm Kanishka" > file.txt
```
2. Stage The file:
```
git add file.txt
```
3. Commit the staged file:
```
git commit -m "yo we are kamineys"
```
### Task 4: Write Effective Commit Messages

1. Create a detailed commit message:
```
git commit -m "Added initial version of file.txt with project overview"
```
2. Commit multiple files with one message:
```
touch file1.txt file2.txt
git add .
git commit -m "Added two new files for feature setup"
```
## Part 3: Viewing Commit History with git log

### Task 5: View Detailed Commit History

1. View full commit logs: Shows a detailed list of commits with hash, author, date, and message.
```
git log
```
2. View commit history in a compact format:
```
git log --oneline
```
### Task 6: Customize Log Outputs

1. View logs with a graphical representation:
```
git log --oneline --graph --decorate
```
2. Filter logs for specific files:
```
git log file.txt
```
## Part 4: Understanding Branching and Merging

### Task 7: Understanding Branching

1. List all branches:This gives the list of all the active branches.
```
git branch
```
2. Create a new branch: It creates a new branches without switching to it.
```
git branch new-branch
```
3. Switching to a new branch:
```
git checkout new-branch
```
* Alternative Method:
```
git checkout -b new-branch
```
This method creates a new branch and stwitches to it.

## Part 5: Creating and Working with Branches

### Task 8: Make Changes in a Branch

1. Add content to a file in the new branch:
```
echo "Feature in progress" > feature.txt
git add feature.txt
git commit -m "Added feature.txt in new-branch"
```
### Task 9: Merging Branches

1. Switch back to the main branch:
```
git checkout main
```
2. Merge the ```new-branch``` to the ```main``` branch:
```
git merge new-branch
```
## Part 6: Resolving Merge Conflicts

### Task 10: Simulate a Merge Conflict

1. Modify the same line in a file on two branches:
```
echo "Main branch content" > conflict.txt
git add conflict.txt
git commit -m "Added conflict.txt in main branch"
```
2. Switch to the other branch and make conflicting changes:
```
git checkout new-branch
echo "new-branch content" > conflict.txt
git add conflict.txt
git commit -m "Modified conflict.txt in new-branch"
```
3. Merge ```new-branch``` with ```main```:
```
git checkout main
git merge new-branch
```
4. Resolve the conflict by editing the file and choosing the correct version:
 *  Navigate to the ```conflict.txt``` and descide which changes to keep.
 *  Stage the resolved file:
 ```
 git add conflict.txt
 ```
 *  Commit the merge:
 ```
 git commit -m "Resolved conflicts in conflict.txt"
 ```
 ## Part 7: Deleting and Renaming Branches

 ### Task 11: Delete a Branch

 1. Delete a  local branch:
 ```
 git branch -d new-branch
 ```
 2. Force-delete a branch: It deletes the branch even if it isn't merged.
 ```
 git branch -D new-branch
 ```
 ### Task 12: Rename a Branch

 1. Rename the current branch:
 ```
 git branch -m new-branch-name
 ```
 2. Rename another branch which is not checked out:
 ```
 git branch old-branch-name new-branch-name
 ```
 