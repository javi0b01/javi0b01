# :memo: Notes
## GIT
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Git](https://git-scm.com/)
- [Git Reference Manual](https://git-scm.com/docs)
- [Pro Git book](https://git-scm.com/book)
- [Git Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
* [GitHub](https://github.com/)
  - [Managing remote repositories](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories)
- [GitLab](https://gitlab.com/)
- [Bitbucket](https://bitbucket.org/)
- [Azure Repos](https://azure.microsoft.com/en-us/products/devops/repos)
- [git-flow cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)
- [Multiple Accounts and SSH Keys](https://dbushell.com/2013/01/27/multiple-accounts-and-ssh-keys/)
- [tj/git-extras](https://github.com/tj/git-extras)
#### Open Source Project
- https://forgoodfirstissue.github.com/
- https://goodfirstissue.dev/
- https://goodfirstissues.com/
### Terms and concepts
- Git SCM (Source Code Management)
* Version Control System (local)
  - Installation
  - Configuration
* Version Control Hosting (remote)
  - Sign up
  - Clone
  - Remote
  - Tokens
  - Fetch
  - Merge
  - Pull
  - Push
  - Fork
  - Rebase
* Repository
  - Local
  - Remote
  - Clone
  - Fork
  - Pull request
  - Issues
* Repository
  - Initialize
  - Delete
* Repository
  * Areas or Flow
    - Working directory
    - Preparation area or staging area
    - Repo
    * .git directory or core or repository
      - Metadata
      - All versions
  * Status (A specific version of the file)
    - Modified
    - Staged or prepared
    - Committed or confirmed
- CLI
- Tracking
- Status
- Add
- Unstage
* Commit
  - Timeline, status record
  - SHA ID or Secure Hash Algorithm ID
  - User
  - Email
  - Date
  - Custom message
- History
- Change last commit message
- Undo last commit
* Branch
  - Independent line of development
- Merge
- Conflicts
* Files
  - README
  - gitignore
  - CONTRIBUTING
  - LICENSE
### Setup
```
$ sudo apt install git-all
$ sudo apt-get install install-info
$ git --version
$ git config --global init.defaultBranch <name>
$ git config --global credential.helper store
$ git config --global user.name "<name>"
$ git config --global user.email <email>
$ git config --global core.editor "<editor --flag>"
$ git config --global core.editor "<code --wait>"
$ git config --global -e
$ git config --global core.autocrlf <input/true>
$ git config --global color.ui <true/false/always/auto>
$ git config --global color.branch <true/false/always>
$ git config --global color.diff <true/false/always>
$ git config --global color.interactive <true/false/always>
$ git config --global color.status <true/false/always>
$ git config --list
$ git config --h
```
Basics
```
$ git init
$ git remote add origin <REMOTE URL>
$ git push origin <BRANCH NAME>
$ git status
$ git status -s
$ git add
$ git rm --cached <FILE NAME>
$ git restore <FILE NAME>
$ git commit -m
$ git diff
$ git log
$ git log --oneline
$ git branch
$ git checkout
$ git switch
$ git switch -c
$ git merge <BRANCH NAME>
$ git push
$ git pull
```
### COMMANDS
Branch
```
$ git branch
$ git branch -a
$ git branch -r
$ git branch <name>
$ git branch --set-upstream-to=<remote>/<branch name> <branch name>
$ git checkout -b <branch name>
$ git checkout <branch name>
$ git branch -m <current name> <new name>
$ git branch -m <new name>
$ git push --set-upstream origin <branch name>
$ git branch -d <branch name>
$ git branch -D <branch name>
$ git push origin --delete <branch name>
$ git branch -a
$ git checkout -b <new local branch name> origin/<remote branch name>
$ git checkout -t origin/<remote branch name>
$ git switch <BRANCH NAME>
$ git switch -c <BRANCH NAME>
$ git pull
```
History
```
$ git log
$ git log --oneline
$ git log --p
$ git log --author="<user name>"
$ git log --since=1.month.ago --until=1.day.ago
$ git log --pretty="format:%h %s"
$ git restore --source <id>
```
Tagging
```
$ git tag
$ git tag <tag name>
$ git describe --tag
$ git push --tag
$ git push --delete origin <tag name>
$ git tag -d <tag name>
```
Basic
```
$ git clone <REMOTE_URL>
$ git clone <REMOTE_URL> <DIRECTORY>
$ git clone <REMOTE_URL> --depth=1
$ git status
$ git add
$ git add <filename>
$ git rm <filename>
$ git commit -m <description>
$ git commit <see text editor>
$ git commit --amend -m <description>
$ git commit --amend <see text editor>
$ git reset --soft HEAD~1
$ git reset --hard HEAD~1
$ git push
$ git push -u origin <BRANCH NAME>
$ git push origin <BRANCH NAME>
$ git fetch
$ git merge
$ git merge --continue
$ git pull
$ git log

$ git revert <COMMIT-HASH>
$ git stash
$ git stash list
$ git stash pop
$ git reset --hard <COMMIT-HASH>
$ git push --force origin <BRANCH NAME>

$ git tree
```
Fecth
```
$ git fetch
$ git fetch <REMOTE BRANCH>
$ git fetch --all
$ git log --oneline --all
$ git log --oneline <LOCAL BRANCH>..<REMOTE BRANCH>
$ git merge <ORIGIN BRANCH>
$ git push
```
Remote
```
$ git remote
$ git remote --verbose
$ git remote -v
$ git pull
$ git fetch
$ git checkout origin/main
$ git push

$ git remote add upstream <REMOTE_URL>
$ git pull upstream <BRANCH NAME>
```
Rebase
```
$ git rebase -i <commit> or git rebase --interactive <commit>
$ git push or git push --force-with-lease
```
Create a new repository on the command line
```
$ echo '# repo-name' > README.md
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin <REMOTE_URL>
$ git push -u origin main
```
Push an existing repository from the command line
```
$ git remote add origin <REMOTE_URL>
$ git branch -M main
$ git push -u origin main
```
Adding a local repository to Git
```
$ git init -b main
$ echo '# repo-name' > README.md
$ git add . && git commit -m "initial commit"
$ git remote add origin <REMOTE_URL>
$ git remote -v
$ git push origin main
```
Switch to a remote Git branch that isn't local
```
$ git branch -r
$ git fetch
$ git checkout <branch name>
$ git status
```
More
```
$ git checkout
$ git init
$ git rm --cached <filename>
$ git rm --force <filename>
$ git commit
$ git commit -a <description>
$ git commit -am <description>
$ git show
$ git log --stat
$ git diff
$ git diff <id> <id>
$ git reset
$ git reset --hard
$ git reset --hard <COMMIT HASH>
$ git reset <id>
$ git reset <id> --soft
$ git reset <id> --hard
$ git reset HEAD
$ git fetch
$ git stash
$ git clean
$ git reflog
$ git reset
$ git remote
$ git remote -v
$ git remote add upstream
$ git show
$ gitk
```
Git Extras
```
$ sudo apt-get install git-extras
$ git extras --version
$ git extras --help
$ git extras update
$ git info
$ git count
$ git count --all
$ git effort
$ git effort --above 15
$ git effort -- --since='last month'
```
Config file
```
Host github.com
  HostName github.com
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host gitlab.com
  HostName gitlab.com
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host bitbucket.org
  HostName bitbucket.org
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host bitbucket-<SECONDARY ACCOUNT>
  HostName bitbucket.org
  User git
  PreferredAuthentications publickey
  IdentitiesOnly yes
  IdentityFile ~/.ssh/<SECONDARY KEY>
```
Bitbucket - App passwords
```
$ git remote set-url origin https://USERNAME:APP_PASSWORD@bitbucket.org/WORKSPACE/REPO.git
```
GitHub CLI
```
gh repo clone <REMOTE_URL>
```
### Git Branching
1. A **develop** branch is created from **main**
2. A *release* branch is created from **develop** `release/vX.X.X`
3. *feature* branches are created from **develop** `feature/myfeature`
4. When a *feature* is complete it is merged into the **develop** branch
5. When the *release* branch is done it is merged into **develop** and **main**
6. If an issue in **main** is detected a *hotfix* branch is created from **main** `hotfix/myfix`
7. Once the *hotfix* is complete it is merged to both **develop** and **main**

### Generic Commit Messages
- Update README file
#### General Purpose
- chore: general cleanup
- refactor: improve code structure
- fix: minor bug fix
- feat: add new feature
- update: general update
- docs: update documentation
- style: format code
- test: add/update tests
#### Development Progress
- wip: work in progress
- init: initial commit
- temp: temporary changes
- debug: add debug logs
- remove: delete unused code
#### Deployment & Releases
- release: prepare for release
- build: update build scripts
- ci: update CI config
#### Dependency Management
- deps: update dependencies
- deps: bump package versions
- deps: remove unused packages
#### Cleanup & Maintenance
- cleanup: remove unused files
- optimize: improve performance
- config: update configuration
#### Top Generic Git Commit Messages
- init: initial project setup
- feat: add new feature
- fix: resolve bug in [feature/module]
- refactor: improve code structure
- style: format code and clean up
- docs: update README or documentation
- test: add or update tests
- chore: general maintenance tasks
- build: update build configuration
- release: prepare for version release
---
- init: initial project setup
- feat: add new feature
- fix: minor bug fix
- refactor: improve code structure
- style: format code
- docs: update documentation
- test: add or update tests
- chore: general cleanup
- build: update build configuration
- release: prepare for version release
- update: general update
- wip: work in progress
- temp: temporary changes
- debug: add debug logs
- remove: delete unused code
- ci: update CI config
- deps: update dependencies
- cleanup: remove unused files
- optimize: improve performance
- config: update configuration

## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
