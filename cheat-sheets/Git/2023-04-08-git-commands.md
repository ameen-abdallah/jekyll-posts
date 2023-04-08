---
layout: post
title: Git commands
date: 2023-04-08 16:28 +0200
categories: [Cheat sheets, Git]
tags: [cheat sheets, git, git remote] 
---
## Initializing a folder
### init
This command turns a directory into an empty Git repository. This is the first step in creating a repository. After running git init, adding and committing files/directories is possible.

Usage:

```shell
git init
```
## Adding files and committing
### add
Adds files in the to the staging area for Git. Before a file is available to commit to a repository, the file needs to be added to the Git index (staging area). There are a few different ways to use git add, by adding entire directories, specific files, or all unstaged files.

Usage:

```shell
git add <file or directory name>
```
### commit
Record the changes made to the files to a local repository. For easy reference, each commit has a unique ID.

Usage:

```shell
git commit -m "Commit message in quotes"
```
### status
This command returns the current state of the repository.

Usage:

```shell
git status
```
## Connecting with a remote repository
### remote
To connect a local repository with a remote repository. A remote repository can have a name set to avoid having to remember the URL of the repository.

Usage:

```shell
git remote <command> <remote_name> <remote_URL>

git remote -v
```

## Cloning, pulling and pushing to remote repositories
### clone
To create a local working copy of an existing remote repository, use _git clone_ to copy and download the repository to a computer. Cloning is the equivalent of _git init_ when working with a remote repository. Git will create a directory locally with all files and repository history.

Usage:

```shell
git clone <remote_URL>
```

In Practice:

```shell
git clone git@account_name.git.beanstalkapp.com:/acccount_name/repository_name.git
```

### pull
To get the latest version of a repository run _git pull_. This pulls the changes from the remote repository to the local computer.

Usage:

```shell
git pull <branch_name> <remote_URL/remote_name>
```

### git push
Sends local commits to the remote repository. _git push_ requires two parameters: the remote repository and the branch that the push is for.

Usage:

```shell
git push <remote_URL/remote_name> <branch>

# Push all local branches to remote repository
git push —all
```