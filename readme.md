## Git Basics

Git tracks changes through three stages
* Working directory  
* Index aka. Staging
* HEAD  

Working directory is all the files in the local repo in their current state.  
None of these files are tracked by git.  
Use `git add` to add these files to staging. Can add single or multiple files with `git add file1.txt file2.txt`, all the files of type with `git add *.txt` or all the files with `git add .` 
Use `git commit` to move these files to an official version in the HEAD. The HEAD is the most recent version of your code.  
Use `git push` to move these files to github.
___
Use `git pull` to get all of the changes from the repo to your computer
Use `git status` to see the status of the working directory in the staging area. Use `git status -s` for short status.
Use `git diff` to see differences not added to index/staging
*View help with `git --help`*


## Branches
Create a new branch with `git branch [branch name]`
Switch to a branch with `git checkout [branch name]` 
*Shortcut to create and switch at the same time with `git checkout -b [branch name]`*
Merge all changes from a branch into your current branch with `git merge [branch name]`

## Log 
View history with `git log`
View history on oneline with `git log --oneline` or `git log --oneline --reverse`

## Initialize a repository
git init

## Restore
Use restore to unstage files
`git restore --staged file1.js` or `git restore --staged .`

Remove file from working directory and the staging area
`git rm file1.js`

## Rebase
Rebase is the process of taking a current branch and moving it's base point to the end of the master branch.
Don't rebase a shared feature branch. This will lead to a lot of merge conflicts.

      A---B---C feature
     /
D---E---F---G master

to

              A---B---C feature
             /
D---E---F---G master


## Squash
Squashing takes a series of commits and squashes them into a single commmit.

## Squash rebase workflow
https://blog.carbonfive.com/always-squash-and-rebase-your-git-commits/
Before you merge a feature branch back into your master branch, your feature branch should be squashed down to a single buildable commit, and then rebased from the up-to-date main branch.