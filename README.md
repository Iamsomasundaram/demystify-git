# Demystify Git

### You can refer the following links to learn Git

- https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud
- https://youtu.be/8KCQe9Pm1kg
- https://youtu.be/2sjqTHE0zok

### Few popular books to refer

| [<img src="https://user-images.githubusercontent.com/45349552/223785088-9aae19b6-3b2a-4877-9b2c-daa1b2000eff.png" width="150">](https://git-scm.com/book/en/v2) | [<img src="https://user-images.githubusercontent.com/45349552/235899467-ba85628c-4141-457f-b9e3-adb846cd1868.png" width="150">](https://www.amazon.com/Professional-Git-Brent-Laster/dp/111928497X) | [<img src="https://user-images.githubusercontent.com/45349552/235899821-e7a921ca-01cb-461e-af21-a7edb05afba6.png" width="150">](https://www.amazon.com/Rys-Git-Tutorial-Ryan-Hodson-ebook/dp/B00QFIA5OC) |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

### Few public repos to practice git commands

### Create/Setuping up a repo

| Commands                   | Description                                     |
| -------------------------- | ----------------------------------------------- |
| git init <directory>       | Create empty Git repo in specified directory    |
| git clone <repo>           | Clone repo located at <repo> onto local machine |
| git config --edit          | Update config values                            |
| git config --global --edit | To update name and email                        |

### Browse

| Commands                                                           | Description                                                                            |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| git branch                                                         | List down the branches in your working directory                                       |
| git status                                                         | Files changed in working directory                                                     |
| git status &#124; grep .js$                                        | Filter js files from the git status list. .js can be replaced with any file extensions |
| git status -uno                                                    | Show files changed in working directory but not untracked files                        |
| git log                                                            | History of changes                                                                     |
| git log -p                                                         | Display the full diffs of each commit                                                  |
| git log --author="<pattern>"                                       | Search for commits by a particular author                                              |
| git log --grep="<pattern>"                                         | Search for commits with a commit message that matches <pattern>                        |
| git log --name-status                                              | Show only names and status of changed files                                            |
| git log --stat                                                     | Generate a diffstat                                                                    |
| git log --name-only                                                | Show only names of changed files                                                       |
| git log --no-merges --pretty=medium origin/master..origin/<branch> | To get the list of commits of a branch                                                 |
| git whatchanged --stat                                             | Show logs with difference each commit introduces                                       |
| git show commit_id                                                 | Show various types of objects                                                          |
| git show commit_id:file >file.txt                                  | Write the changes made to a file in a commit hash to a file                            |
| git show commit_id -pretty="format:" --name-only                   | Shows commit info a formatted manner                                                   |
| git show stash_no                                                  | Shows diffs in a stash                                                                 |
| git show branch_name:file                                          | View certain file in a specific branch without checking it out                         |
| git diff branch2...branch1                                         | show the diff of what is in branch1 that is not in branch2                             |
| git diff origin/master --name-only                                 | To get the list of files committed in a branch                                         |
| git blame file                                                     | Who changed what and when in a file                                                    |
| git blame -L1,10 <file_name>                                       | To know who worked from line number 1 to 10                                            |
| git rm file                                                        | Remove file from working directory                                                     |
| git grep                                                           | Search working directory                                                               |

### Revert/Undoing

| Commands                                            | Description                                                              |
| --------------------------------------------------- | ------------------------------------------------------------------------ |
| git reset                                           | Revert your repository to a previous known working state                 |
| git reset --hard                                    | Revert everything to the last commit. you cannot undo a hard reset       |
| git reset file                                      | Remove <file> from the staging area, but it will be in working directory |
| git revert commit_id                                | Reverts commit_id. A new commit is created                               |
| git revert --no-commit                              | Revert the commit but don't commit. Run git status to see the files      |
| git revert -m 1 <merge-commit>                      | Revert merge commit                                                      |
| git checkout file                                   | To revert the changes made to file                                       |
| git checkout master <file_name>                     | Removes the committed changes in file from the branch                    |
| git clean                                           | Remove all untracked directories and the files                           |
| git clean -d -f --dry-run                           | Lists files that would be deleted                                        |
| git clean -d -f                                     | Deletes the untracked files                                              |
| git show commit_id -- file_name &#124; git apply -R | Reverting a file from a commit                                           |
| git apply -R patch.diff                             | Reverting diffs                                                          |

### Useful Commands

| Commands                                            | Description                                                       |
| --------------------------------------------------- | ----------------------------------------------------------------- |
| git command --help                                  | When in doubt, use git help                                       |
| git log --oneline                                   | Show a list of commits in a repository in a more summarised way   |
| git shortlog -s -n                                  | List of authors and commits to a repository sorted alphabetically |
| git commit --amend                                  | To amend the last commit                                          |
| git config --global alias.<new_name> <git_commands> | To create alias                                                   |

### Branch

| Commands                        | Description                                                                                      |
| ------------------------------- | ------------------------------------------------------------------------------------------------ |
| git branch                      | List all local branches                                                                          |
| git branch -a                   | List all branches, local and remote                                                              |
| git branch --contains commit_id | To check whether the branch has that commit                                                      |
| git branch -m <new_branch_name> | Rename the current branch to <new_branch_name>                                                   |
| git checkout _branch_name_      | Switch to a branch, branch_name                                                                  |
| git merge branch2               | Merges branch2 with your current branch                                                          |
| git checkout -b _new_branch_    | Creates branch named new_branch from your current branch                                         |
| git branch _new_branch_         | Create branch named new_branch based on the HEAD                                                 |
| git branch -d branch_name       | Remove selected branch, if it is already merged into any other. -D instead of -d forces deletion |

### Publish

| Commands                              | Description                                                          |
| ------------------------------------- | -------------------------------------------------------------------- |
| git status                            | Displays the state of the working directory                          |
| git diff files                        | To see the changes made on a file                                    |
| git diff --staged [files]             | To see the changes made on a staged file                             |
| git diff --cached [files]             | Same as above                                                        |
| git diff -R origin/master...HEAD      | Reverse patch                                                        |
| git add files                         | Adds a change in the working directory to the staging area           |
| git add -u                            | Staging all modified tracked files                                   |
| git add .                             | Staging both tracked and untracked files under the current directory |
| git commit files -m "Commit Message"  | Commit your files                                                    |
| git push                              | Push local changes to the origin                                     |
| git push -d origin <branch_name>      | Delete branch in remote repostry                                     |
| git cherry-pick commit_id             | Pick a commit from one branch and apply it onto another              |
| git cherry-pick commit_id --no-commit | Pick a commit from one branch and apply it onto another dont commit  |

### Synchronize/Update

| Commands  | Description                                                                       |
| --------- | --------------------------------------------------------------------------------- |
| git fetch | To download contents from a remote repository                                     |
| git pull  | To update your current HEAD branch with the latest changes from the remote server |

### Temporary store

| Commands                                   | Description                                                             |
| ------------------------------------------ | ----------------------------------------------------------------------- |
| git stash save                             | Save modified and staged changes                                        |
| git stash list                             | List stack-order of stashed file changes                                |
| git stash list --date=local                | Gets stash created date                                                 |
| git stash pop                              | Write working from top of stash stack                                   |
| git stash apply stash_no                   | Applies the given stash                                                 |
| git show stash_no                          | To see the changes in a stash                                           |
| git stash show -p stash_no                 | Show this particular stashed content without applying it                |
| git stash drop stash_no                    | Removes specific stash from list                                        |
| git stash drop                             | Discard the changes from top of stash stack                             |
| git stash -u/git stash --include-untracked | Command lets us stash untracked files and doesn't touches ignored files |
| git stash --all                            | Stashes all untracked and ignored files                                 |

### Conflicts

| Commands | Description |
| -------- | ----------- |
| git diff --name-only --diff-filter=U | Show conflicted files alone |
| git log --merge | Produce a log with a list of commits that conflict between the merging branches |
| git merge --abort | To abort merge process |
| git merge --no-commit | To simply prevent the merge commit to occur |

