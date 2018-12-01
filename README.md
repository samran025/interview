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
| git remote add origin url | will add the new  remote  Before adding the remote you have to create the required repository in your git service |
| git remote  | list all the exiting redmote with the repository |
| git remote -v  | list all the exiting redmote with the repository with url |


root@kali2:~/git_training/.git# cat config
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
[remote "origin"]
        url = https://github.com/samran025/test.git
        fetch = +refs/heads/*:refs/remotes/origin/*

root@kali2:~/git_training/interview# git remote

origin

root@kali2:~/git_training/interview# git remote -v

origin  https://github.com/samran025/interview.git (fetch)

origin  https://github.com/samran025/interview.git (push)


| Command | Description |
| --- | --- |
| git config --global user.name "  " | saves the config in $HOME/.gitconfig |
| git config --global alias.c "clone url" | aliasing the command and saves the config in $HOME/.gitconfig |
| git config  user.name "  " | saves the config in $GITDIR/.gitconfig |


root@kali2:~# cat .gitconfig

[user]

        name = samran025


| Command | Description |
| --- | --- |
| git checkout -b "branch_name" | creates a branch |
| git push --set-upstream remote_name "branch_name" | creats a branch in remote repo |



| Command | Description |
| --- | --- |
| git add . | stage the file |
| git rm . | remove the file from remote |


Gitingonre

we can use .gitingonre : the files and directory that we don't want to share
files conatining : passwords,login info ,conf

When a file or directory is ignored, it will not be:
1. tracked by Git
2. reported by commands such as git status or git diff
3. staged with commands such as git add -A

by adding in .gitignore
or .git/info/exclude


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

root@kali2:~/git_training/interview# git shortlog -s

     3  root
     4  samran025


root@kali2:~/git_training/interview# git shortlog
root (3):
      command
      command2
      command3

samran025 (4):
      Create README.md
      Update README.md
      b
      bb
      

root@kali2:~/git_training/interview# git log -2 --oneline
46174e5 bb
f228c68 b



git log master..foo will show the commits that are on foo and not on master. Helpful for seeing what commits
you've added since branching!


Clear already committed files, but included in .gitignore
root@kali2:~/git_training/test# echo "README.md" >.gitignore
root@kali2:~/git_training/test# git status
# On branch git
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#       modified:   README.md
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       .gitignore
no changes added to commit (use "git add" and/or "git commit -a")

root@kali2:~/git_training/test# git rm -r --cached .
rm 'README.md'
rm 'a.xls'
rm 'cmd.csv'
rm 'tests-example.xls'
root@kali2:~/git_training/test# ls
a.xls  cmd.csv  README.md  tests-example.xls
root@kali2:~/git_training/test# git status
# On branch git
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       deleted:    README.md
#       deleted:    a.xls
#       deleted:    cmd.csv
#       deleted:    tests-example.xls
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       .gitignore
#       a.xls
#       cmd.csv
#       tests-example.xls
        
To fix this problem, one could perform a "dry-run" removal of everything in the repository, followed by re-adding all
the files back. As long as you don't have pending changes and the --cached parameter is passed, this command is
fairly safe to run
