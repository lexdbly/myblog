---
title: "Starting with Hugo"
date: 2020-12-09T22:32:27+11:00
tags:
    - hugo
    - golang
categories:
    - tech
keywords:
    - hugo
    - golang
    - go
draft: false
---

I decided to abandon Wordpress for good, and move my everything to [hugo](https://gohugo.io/).
Hugo is a static site generator written in Go language. Saying that, I have no clue about Go lang or any static site generators.
Nevertheless, I managed to build this site and it does not look too bad in the end, does it?

I'd like to show you how to install hugo and deploy your website by using hugo, github and digitalocean. Lets get started!

# Install Hugo on MacOS

Install hugo via terminal
```bash
brew install hugo # install hugo
which hugo # verify your installation -> /usr/local/bin/hugo
hugo version # check version -> Hugo Static Site Generator v0.13 BuildDate: 2015-03-09T21:34:47-05:00
```

Create a new site in current directory
```bash
hugo new site YOURFOLDERNAME # change YOURFOLDERNAME
```

## Themes

You need to pick a theme from [Hugo's theme library](https://themes.gohugo.io/) (unless you want to write your own).

Each theme has a sample site inside and you will be able to customise your theme by using *config.toml* file in the sample site folder.

Hugo's folder structure looks like this:

```bash
- YourHugoProject
--- archetypes
--- content
--- data
--- layouts
--- resources
--- static
--- themes
--- config.toml
```

TBC...