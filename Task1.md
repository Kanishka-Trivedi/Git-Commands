## Part 1: Introduction to Version Control and Git
### Task 1: Install and Configure Git

1. Configure Git with your username and email:
```
git config --global user.name "Kanishka Trivedi"
git config --global user.email "kally651997@gmail.com"
```
2. View your Git configuration:
```
git config --list
```
### Task 2: Initialize a Repository

1. Create a new project folder and navigate to it:
```
mkdir MyProject
cd MyProject
```
2. Initialize it as a Git repository:
```
git init
```
### Task 3: Create a File and Make Multiple Commits

1. Create a new file and add content:
```
echo "My First Project" > README.md
```
2. Stage the file:
```
git add README.md
```
3. Commit the file:
```
git commit -m "Initial commit: Added README.md"
```
4. Make changes to the file:
```
echo "Added a description" >> README.md
```
5. Stage and commit the changes:
```
git add README.md
git commit -m "Updated README with a description"
```
### Task 4: Check Status and Log

1. Check the repository’s current status:
```
git status
```
2. View commit history in detail:
```
git log --oneline --graph --decorate
```
Example Output:
```
* 2f8d6a2 (HEAD -> main) Updated README with a description
* d3c4b21 Initial commit: Added README.md
```
### Task 5: Create and Clone a Repository

1. Create a repository on GitHub named ```example-repo```.
2. Clone it locally:
```
git clone http://codinggita.com/example-repo
```
### Task 6: Understanding the Git Workflow

 * Example Workflow:

 i. Make changes to a file in the **working directory**:
 ```
 echo "Workflow example" > workflow.md
 ```
 ii. Stage the file:
 ```
 git add workflow.md
 ```
 iii. Commit the file to the repository:
 ```
 git commit -m "Added workflow example"
 ```

## Part 2: Working with Repositories
### Task 7: Branching and Merging
1. Create a new branch for a feature:
```
git branch feature-login
git checkout feature-login
```
  Or Use:
```
git branch -b checkout feature-login
```
2. Add a new file and commit changes:
```
echo "Login Page" > login.html
git add login.html
git commit -m "Added login page"
```
3. Merge the feature branch into ```main```:
```
git checkout main
git merge feature-login
```
### Task 8: Handling Merge Conflicts
1. Create two branches:
```
git branch branch-A
git branch branch-B
```
2. Modify the same line in ```README.md``` in both branches.
3. Merge ```branch-A``` into ```main```:
```
git checkout main
git merge branch-A
```
4. Attempt to merge ```branch-B``` into ```main```(This will use a conflict):
```
git merge branch-B
```
5. Resolve the conflict manually in ```README.md```, then:
```
git add README.md
git commit -m "Resolved merge conflict between branch-A and branch-B"
```
### Task 9: Renaming and Deleting Branches

1. Rename a branch:
```
git branch -m old-branch-name new-branch-name
```
2. Delete a branch:
```
git branch -d feature-login
```

## Part 3: Advanced Git Operations
### Task 10: Using Git Stash
Stash is used when we add or make changes but don't commit it but save it for later.

1. Make changes to a file but don’t commit:
```
echo "Temporary work" >> temp.md
```
2. Stash the changes:
```
git stash
```
3. View stashed changes:
```
git stash list
```
4. Apply the stashed changes:
```
git stash apply
```
5. Drop the stash after applying:
```
git stash drop
```

### Task 11: Rewriting History with Interactive Rebase

1. Create multiple commits.
```
echo "Commit1" >> file1.txt && git add file1.txt && git commit -m"Commit1"
echo "Commit2" >> file2.txt && git add file2.txt && git commit -m"Commit2"
echo "Commit3" >> file3.txt && git add file3.txt && git commit -m"Commit3"
```
2. Squash commits into one.
```
git rebase -i HEAD~3
```
### Task 12: Cherry-Picking Commits

1. Create a new branch.
```
git checkout -b cherry-pick-example
```
2. Cherry-pick a specific commit from another branch:
```
git cherry-pick <commit-hash>
```
### Task 13: Tagging Commits
1. Tag the current commit:
```
git tag -a v1.0 -m "Version 1 release"
```
2. Push the tag to the remote repository:
```
git push origin v1.0
```

### Task 14: Working with Remote Repositories
1. Add a remote repository:
```
git remote add origin <repo link>
```
2. Push your changes to the remote repository:
```
git push origin main
```

### Task 15: Forking and Contributing
1. Fork a repository on github.
2. Clone the fork locally:
```
git clone <forked-repo-link>
```
3. Create a new branch ,make changes and then push.
```
git checkout -b fix-typo
echo "typo-fixed" >> README.md
git add README.md
git commit -m "Fixed typo"
git push origin fix-typo
```
4. Open the pull request on github.

## Part 4: Additional Practice
### Task 16: Simulate Team Collaboration

1. Create a repository and share it with a friend.
2. Both make changes to the same file simultaniously.
3. Practice resolving merge conflicts and pushing changes.

### Task 17: Git Ignore
1. Create a ```.gitignore``` file:
``` 
echo "node_modules/" > .gitignore
```
2. Add files to ensure the ignored files are not added.
```
git add .
```
