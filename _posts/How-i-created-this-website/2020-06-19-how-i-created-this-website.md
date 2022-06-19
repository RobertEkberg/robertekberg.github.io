---
title: How i created github pages website
date: 2022-06-19 10:01:47 +07:00
modified: 2022-06-19 18:49:47 +07:00
tags: [ruby, jekyll, github, website development]
description: Here you can read how i created my own blog with github pages, jekyll, and ruby.
image: assets/img/repository-github-pages-jekyll.png
---

If you want to create a github pages website you need to have ruby and jekyll installed (I created my website on windows).

## SETTING UP THE REPOSITORY

Choose your repository name where you will have your github pages website.
Press create repository then go to repository settings.

<img src="{{site.baseurl}}../assets/img/repository-github-pages-jekyll.png">

Go to source, then change the source to be master branch. Below, you can also change the theme if you want, normally the standard theme will be minima.

You can now visit your website. Your website url will be **repositoryname.github.io**.

(ignore the custom domain for now)

<img src="{{site.baseurl}}../assets/img/repository-settings.png">

## CONFIGURING OUT WEBSITE

In order to configure your website, you need to download VSCode (Visual Studio Code).

One you have downloaded VSCode and opened it, press ctrl + shift + p, and type “git clone”.

Choose a folder where you want the content of the repository to be located on your computer.

<img src="{{site.baseurl}}../assets/img/vscode-clone.png">

Open a new terminal and type the command 

Jekyll new . -–force
(this will install jekyll library to the folder)

bundle exec jekyll serve
(This will host your website locally)

You can now press ctrl + shift +
p, and type "git commit" and you will you will upload changes you made locally on your computer to the repository.

 <img src="{{site.baseurl}}../assets/img/vscode-commit-sync.png">

Now you can edit and update your website.

You can create new posts by copying already existing blog posts in the _posts folder.