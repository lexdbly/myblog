---
title: "Starting with Git"
date: 2020-12-10T12:50:13+11:00
tags:
    - git
    - VCS
    - versioncontrol
    -tutorial
categories:
    - tech
keywords:
    - git
    - version control system
    - cheatsheet
draft: false
---

Start here:
- [Cheatsheet](https://cdn.rawgit.com/hostinger/banners/cc2e0268/tutorials/pdf/GIT-cheat-sheet.pdf)
- [Another cheatsheet](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)
- [And another one](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

# Command list

## Install Git on MacOS

Install Git using Homebrew
```bash
brew install git
git version
```

Move to root directory and initialize Git
```bash
git init
git init [PROJECT NAME]
```

## Prepare working directory

Clone a repository from remote or local server
```bash
git clone username@host:/path/to/repo #remote server

git clone /path/to/repo #local server
```

Add files to staging area
```bash
git add [filename.ext] #adding a single file
git add [FOLDER/] #adding a folder
git add -p
git add --all .
```

Remove files from staging area
```bash
git rm [filename.ext] #removing a single file
```

Capture changes and save to the Git directory
```bash
git commit -m "commit comment" #commit directly without text editor, with comments
git commit -a #commit all changes in working dir
git commit -am "commit comment" #combination of above two commands
git commit --amend
```

## Working with remote environment

Add remote origin
```bash
git remote add origin <host-or-remoteURL>
# In Git, "origin" is a shorthand name for the remote repository that a project was originally cloned from. More precisely, it is used instead of that original repository's URL

git remote add origin https://www.github.com/your-username/your-repo.git #example github connection

```

Remove remote origin
```bash
git remote rm <name-of-the-repository>
```

Push from staging area to origin
```bash
git push origin <master>

# In Git, "master" is a naming convention for a branch. After cloning (downloading) a project from a remote server, the resulting local repository has a single local branch: the so-called "master" branch. This means that "master" can be seen as a repository's "default" branch.
```

## Customize Git

Configure Git profile
```bash
git config --global user.email "youremail@example.com" #global|local|system
```

Modify Git colors
```bash
git config --global color.ui false|auto|always
```

## What is next?

Following commands to be explained
```bash
git status
git remote –v
git branch
git pull
git merge <branch-name>
git fetch origin
```