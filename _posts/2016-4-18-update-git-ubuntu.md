---
layout: post
published: true
exacttime: "21:35:00"
title: "Update Git on Ubuntu"
category: "ubuntu"
headimg_url: "/images/ubuntu/ubuntu.jpg"
author: thepulkitagarwal
---

Today, I read an [article titled "Remote code execution, git, and OS X"](https://rachelbythebay.com/w/2016/04/17/unprotected/), and as soon as I read it, I checked the version of git on my computer using `git --version`.

`git version 1.9.1`

Okay, but what is the latest version? I googled it, and it was somewhere around 2.8.x. And that was really weird. I keep updating all the time, and yet, this gap was somehow there. Try it, and if you are on Ubuntu, even you will probably have the same problem.

As I soon found out, it is because of the fact that the git repository on the default Ubuntu PPA isn't maintained. The maintained git version is on another PPA. To update to the new PPA, do this:

{% gist thepulkitagarwal/c58e28f612d7f99ea1d63362d2c04168 %}

Checking the version again, I got: `git version 2.8.1`

You should seriously consider updating git. There are a lot of security flaws that have been fixed, some of which are really dangerous. [Read [this](https://rachelbythebay.com/w/2016/04/17/unprotected/) for more]
