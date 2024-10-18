
# Git & GitHub Tutorial By Umer Ali

Welcome to this tutorial on using Git and GitHub! This guide will walk you through essential Git commands and how to interact with GitHub for version control and collaboration.

---

## Table of Contents

1. [Install Git](#install-git)
2. [Configure Git](#configure-git)
3. [Create a Local Repository](#create-a-local-repository)
4. [Add Files to the Repository](#add-files-to-the-repository)
5. [Commit Changes](#commit-changes)
6. [Create and Link Remote Repository](#create-and-link-remote-repository)
7. [Push Changes to Remote](#push-changes-to-remote)
8. [Working with Branches](#working-with-branches)
9. [Undoing Changes](#undoing-changes)
10. [Using .gitignore](#using-gitignore)
11. [Forking and Contributing](#forking-and-contributing)

---

## Install Git

### Check Git Version

Before you start using Git, ensure that it’s installed on your system:

```bash
git --version
```

## SetUp Git(One-time Setup):
Git requires you to set up your user identity for tracking purposes.

## Git Configuration:
```bash
git config --global user.name "username"
git config --global user.email "email"
```
## check configuration :
Check your Git configuration details:
```bash
git config --global --list
```
## Create local Repository:

To create a new Git repository locally, navigate to your project folder and run:

```bash
git init
```
## Add File to the Repository:

To start tracking a specific file:

```bash
git add filename
```
-- To add all the files:

```bash
git add .
```
## Check status of the files:

View the status of files in the repository (whether they are staged, unstaged, or untracked):

```bash
git status
```
## Commit changes:

Once files are staged, commit them to the repository with a descriptive message:

```bash
git commit -m "message to be commited"
```
# Create the remote repository Through the terminal:

Using GitHub CLI, log in and create a new repository:


```bash
gh auth login
gh create repo repositry-name --public
gh create repo repository-name --private
```

## Link your local repo to the remote repository:

Once the remote repository is created, link it to your local repository:

```bash
git remote add origin https://github.com/username/repository-name.git
```
## Push local files to the remote repository:

To upload your changes from the local repository to GitHub, push to the desired branch:

```bash
git push origin branch-name
```
## Rename the branch name:
```bash
git branch -M master main
```
-- change the branch from master to main.


## Push files with only one time branch mentioning
```bash
git push -u origin main
```
## Take changes from the remote repository to the local :

To sync your local repository with the remote one:

```bash
git pull origin branch-name
```
## Check the commit changes history:
```bash
git log
```
# Branches:

## Create branch:

Branching allows you to create new features or fix bugs without affecting the main branch:

```bash
git checkout -b new-branch-name
```
## Switches between branches:

To switch back to another branch:

```bash
git checkout branch-name
```
## Merge 2 Branches:

To merge changes from one branch into the current branch:

```bash
git merge branch-name
```
This will merge the branch you mention to your current branch.

## Delete Branch:

After merging, if you no longer need the branch, you can delete it:

```bash
git branch -d branch-name
```
## Undo Changes:
-- To unchange the files:
```bash
git reset file-name
```
## Undo all changes(not commited yet):
```bash
git checkout --filename
```
## Adding .gitignore file

-- gitignore file not push unneccessary files to your remote repo.
for example:
```bash
.env
node_module/`
```
# Push to remote repo (first time ever):
 
 If this is your first push to a new repository, you may need to set the upstream branch:
 
```bash
git push --set-upstream origin main
```
# Forking and Contributing to Other Repositories
To contribute to other repositories:

- Fork the repository on GitHub.
- Clone your fork locally.
- Make your changes and commit.
- Push your changes to your forked repository.
- Create a Pull Request to the original repository.
