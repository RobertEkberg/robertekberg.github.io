---
title: How i created github pages website
date: 2022-06-19 10:01:47 +07:00
modified: 2022-06-19 18:49:47 +07:00
tags: [ruby, jekyll, github, website development]
description: Here you can read how i created my own blog with github pages, jekyll, and ruby.
---

## Introduction

I have for a long time been thinking of having my own website posting things I learn and want others to learn. I’m not a developer so I didn't want to create anything complicated. 

I found another blogger who created their blog with github pages, ruby and jekyll, so i gave it a try. I can tell you right now I love it!. It’s the perfect way if you have a little knowledge of HTML and CSS.

This is how you do it.

## Create a git repository on github.com

If you don't already have a [github](https://github.com/) account you can create one. Once you have created your account you need to make a new repository. 

Name the repository the same name you have on github. For example my name is “RobertEkberg” so my repository name would be robertekberg.github.io. 

<img src="{{site.baseurl}}../assets/img/create-repository.png">

When you have created your repository, find repository settings, then go to pages, and change source to **branch: master**.

<img src="{{site.baseurl}}../assets/img/repository-settings-pages-master-branch.png">


## Clone it to your local machine

Install Visual Studio Code (VSCode). [Download Visual Studio Code here](https://code.visualstudio.com/).

Then, open Visual Studio Code (VSCode). Press **shift + ctrl + p** and type **git clone** and navigate to the folder you want to clone your files in the repository to. (I recommend creating a new folder).

<img src="{{site.baseurl}}../assets/img/vscode-clone.png">

## Install ruby and jekyll

### Install Ruby

You can download ruby to your local machine here. [Download Ruby here](https://www.ruby-lang.org/en/downloads/).

### Install Jekyll

To install jekyll to your local website folder type

```
jekyll new . --force
```

If it doesnt work try to add **--force** at the end. This will overwrite files that are in the folder if its needed.

```
bundler update
```
to update gem to latest versions (you might have to erase the **gemfile.lock** to run this command).

```
bundler install
```
Will add the gem and gemfile.lock back after deleting it.

```
bundle exec jekyll serve --livereload
```
This command will let you host your website from your computer, --livereload will let you see changes made to the website in real time (you can find your website at 127.0.0.1:4000).

## Build your website with jekyll

If you have some basic knowledge of HTML and CSS you can know configure your website. If you want to blog you can create new blog posts in _posts folder. You use [markdown](https://www.markdownguide.org/basic-syntax#overview) when you writing your posts and jekyll will build your website in HTML.

## Deploy your website with Jekyll to github pages

To deploy changes made to your website you press **ctrl + shift + p**, then type **git commit** then **git sync**. Your website will take a few minutes to build, but it should be update with the changes you have made.

<img src="{{site.baseurl}}../assets/img/vscode-commit-sync.png">