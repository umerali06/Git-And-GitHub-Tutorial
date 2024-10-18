# Tutorial Git & GitHub:

## Install Git:
Check git Version
``bash
git --version

## SetUp Git(One-time Setup):
Git Configuration:
``bash
git config --global user.name "username"
git config --global user.email "email"

## check configuration :
``bash
git config --global --list

## Create local Repository:

``bash
git init

## Add File to the Repository:
``bash
git add filename

-- To add all the files
``bash
git add .

## Check status of the files:
``bash
git status

## Commit changes:
``bash
git commit -m "message to be commited"

# Create the remote repository Through the terminal:

``bash
gh auth login
gh create repo repositry-name --public
gh create repo repository-name --private


## Link your local repo to the remote repository:
``bash
git remote add origin https://github.com/username/repository-name.git

## Push local files to the remote repository:
``bash
git push origin branch-name

## Rename the branch name:
``bash
git branch -M master main

-- change the branch from master to main.


## Push files with only one time branch mentioning
``bash
git push -u origin main

## Take changes from the remote repository to the local :
``bash
git pull origin branch-name

## Check the commit changes history:
``bash
git log

# Branches:

## Create branch:
``bash
git checkout -b new-branch-name

## Switches between branches:
``bash
git checkout branch-name

## Merge 2 Branches:
``bash
git merge branch-name

-- This will merge the branch you mention to your current branch.

## Delete Branch:
``bash
git branch -d branch-name

## Undo Changes:
-- To unchange the files:
``bash
git reset file-name

## Undo all changes(not commited yet):
git checkout --filename

## Adding .gitignore file

-- gitignore file not push unneccessary files to your remote repo.
for example:
``bash
.env
node_module/

# Push to remote repo (first time ever):
 
 If this is your first push to a new repository, you may need to set the upstream branch:
 
``bash
git push --set-upstream origin main

# Forking and Contributing to Other Repositories
To contribute to other repositories:

- Fork the repository on GitHub.
- Clone your fork locally.
- Make your changes and commit.
- Push your changes to your forked repository.
- Create a Pull Request to the original repository.
