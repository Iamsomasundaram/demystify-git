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

### Useful Commands

### Branch

### Publish

### Synchronize/Update

### Temporary store

### Conflicts
