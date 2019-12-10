# git-training
Intro training for git


## Branching
`git checkout -b` - create and check out a new branch.

`git branch -l` - this will list all branches.

`git branch -a` - this will show all the branches along with the remote branches.

`git branch -av` - this will do the same as above, but also show the last commit message  


## Commiting
`git status` - will show you changed files in red that are not added and those that are added to the next commit.

`git add .` - adds all changed files in your current location in the directory to the commit, this includes subfolders. 

`git add -A` - adds all changes in the repo to the next commit.

`git add <file name here>` - adds specific files to the next commit.

`git commit -m` - creates a new commit and adds a message. 

`git commit --interactive` - this will open up vim, or another text editor, to add your message to the commit 

## Pushing
`git push origin <branch name>` - push your changes up to the branch. Will create the branch on the git server if it isn't already there.

`git push origin head` - This will do the same as above, but it will not work if you don't set your remote HEAD (current branch pointer). Output to with instructions will come up if you try to push  and haven't set it. 

## Pulling 

`git pull <remote name> <branch>` - this does a git fetch(downloads most recent changes to a branch) and merges the changes with into local branch.
`git fetch <remote name> <branch>` - will download the most recent changes, but will not merge them into your local branch. 

## Git Log 

`git log --decorate` - a colorized output of the git commit history 

`git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative` - super fancy output that will show a graphed output 

`git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"` - save the above out put to an alias of `git lg` 