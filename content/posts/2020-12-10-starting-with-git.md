---
title: "Starting with Git"
date: 2020-12-10T12:50:13+11:00
tags:
    - git
    - VCS
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

Move to a directory and initialize Git
```bash
git init
git init [PROJECT NAME]
```

Clone a repository from remote server
```bash
git clone username@host:/path/to/repo

(or copy a local repo)
git clone /path/to/repo
```

Add a file to staging area
```bash
git add [FILENAME.py] | [FOLDER/]
git add -p
git add --all .
```

Capture changes and save to the Git directory
```bash
git commit -m "commit comment" #commit directly without text editor, with comments
git commit -a #commit all changes in working dir
git commit -am "commit comment" #combination of above two commands
git commit --amend
```

Configure Git profile
```bash
git config --global|local|system user.email "youremail@example.com"


```

Modify Git colors
```bash
git config --global color.ui false|auto|always
```

Configure remote origin
```bash
git remote add origin <host-or-remoteURL>

i.e.
git remote add origin https://www.github.com/your-username/your-repo.git

```

Push from staging area to Git
```bash
git push origin <master>
```


Following commands to be explained further:
```bash
git status
git remote –v
git remote rm <name-of-the-repository>
git branch
git pull
git merge <branch-name>
git rm filename.txt
git fetch origin
```