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
comments: true
---

I decided to abandon Wordpress for good, and move my everything to [hugo](https://gohugo.io/).
Hugo is a static site generator written in Go language. Saying that, I have no clue about Go lang or any static site generators.
Nevertheless, I managed to build this site and it does not look too bad in the end, does it?

I'd like to show you how to install hugo and deploy your website by using hugo, github and digitalocean. Lets get started!

# Install Hugo on MacOS

Install hugo via terminal
```bash
which hugo #verify your installation. You should see something like this if you have hugo already installed: /usr/local/bin/hugo
brew install hugo #install hugo
hugo version #check version: Hugo Static Site Generator v0.13 BuildDate: 2015-03-09T21:34:47-05:00
```

Create a new site in current directory
```bash
hugo new site [foldername] #change foldername
```

## Themes

You need to pick a theme from [Hugo's theme library](https://themes.gohugo.io/) (unless you want to write your own).

Each theme has a sample site inside and you will be able to customise your theme by using *config.toml* file in the sample site folder.

Hugo's folder structure looks like this:

```bash
- YourHugoProject
|-- archetypes
|-- content
    |-- posts   #blog posts here
|-- data
|-- layouts     #theme components come here
|-- resources
|-- static      #all static assets
    |-- css         #place css files here
    |-- js          #place javascript files here
    |-- images      #place images here
    |-- lib         #place library files here such as jquery, bootstrap, fontawesome
|-- themes      #external themes to be installed in this directory
|-- config.toml #theme configuration file
```

You need to create your content (posts and pages) in markdown language, which means a [Markdown Snippet Guilde](https://sites.google.com/site/getsnippet/html-1/markdown) can be useful if you are not familiar with it.

Markdown is a language which replaces typical html codes. For example, `<h1></h1>` tag is replaced by `#` symbol in markdown. For full list of notations, [visit here](https://sites.google.com/site/getsnippet/html-1/markdown) .