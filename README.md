Git:

is an open source SCM(source code management) and distributed revision control system
Version Control System (VCS) is a software that helps software developers to work together and maintain a complete history of their work.

benefit
allow the developer to worl simuntaneusly on the code
don't overide the code of other devloper
track history of the work

Following are the types of VCS:
Centralized version control system (CVCS). : connect to internet
Distributed/Decentralized version control system (DVCS). : we can work locallyonce done we can push our code remotely


| Command | Description |
| --- | --- |
| git init | creates the empty new repository which contains all the plumbing and won't create the branch untill commit |


root@kali2:~/git_training/.git# cat config
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true

creates an empty repository and is not linked to any remote repository

| Command | Description |
| --- | --- |
| git commit | will save save your changes later that we can push remote reposistory it 's like snapshot of entire project |
| git git remote add origin url | will add the new  remote  Before adding the remote you have to create the required repository in your git service |


root@kali2:~/git_training/.git# cat config
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
[remote "origin"]
        url = https://github.com/samran025/test.git
        fetch = +refs/heads/*:refs/remotes/origin/*

| Command | Description |
| --- | --- |
| git config --global user.name "  " | saves the config in $HOME/.gitconfig |

root@kali2:~# cat .gitconfig

[user]

        name = samran025


| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
