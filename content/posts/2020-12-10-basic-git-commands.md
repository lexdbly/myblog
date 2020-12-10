---
title: "Basic Git Commands"
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

[Cheatsheet](https://cdn.rawgit.com/hostinger/banners/cc2e0268/tutorials/pdf/GIT-cheat-sheet.pdf)

## Command list

### Start GIT at the current directory

```bash
git init
git init [PROJECT NAME]
```

### Copy a repo from remote server

```bash
git clone username@host:/path/to/repo

(or copy a local repo)
git clone /path/to/repo
```

### Add a file to staging area. You have to provide file path from initialized git directory.

```bash
git add [FILENAME.py] or [FOLDER/]
```

### Capture changes and save to the git directory

```bash
git commit -m "REASON FOR CHANGES"
```

### Following commands to be explained further:

```bash
git config --global user.email youremail@example.com
git status
git push origin <master>
git remote –v
git remote add origin <host-or-remoteURL>
git remote rm <name-of-the-repository>
git branch
git pull
git merge <branch-name>
git rm filename.txt
git fetch origin
```