---
layout: post
published: true
exacttime: "20:31:00"
title: "Installing Miniconda"
category: "Python"
author: shreyashpatodia
---

Greetings everyone !!

This should be a fairly painless one. Python is an incredibly powerful language with fairly simple grammar. It comes with a large number of libraries that allow programmers to do really complex tasks with relatively ligth-weight code. For example the 
[face detection program](/2016/01/16/face-detection.html) that I wrote about in an earlier post using the incredible OpenCV library. But sometimes managing these libraries can be a real pain and you may not be able to import certain libraries even though they are on your computer because they are not included in the path of the packages that python can find or if you have the library installed for the wrong version of python. 

So we need to start off by downloading miniconda off of their official [website](http://conda.pydata.org/docs/). Conda is a package manager that allows for easy installation for python libraries.(Note: it may be advisable to downlaod and install miniconda in the directory of the user you are logged in as). Once you have downloaded miniconda, run the following command:


`bash Miniconda-latest-MacOSX-x86_64.sh`

If you are on Linux then use:

`bash Miniconda-latest-Linux-x86_64.sh`

If the above command does not work for you(it didn't for me) then replace Miniconda-latest-MacOSX-x86_64.sh with the exact name of the file that got downlaoded. 

Restart terminal. Type in:

`conda -V`

This should tell you the version of conda you have installed. Now you can go crazy with downloading python libraries. Some really important ones are scipy, numpy and maybe html5lib. A couple that I am running right now are BeauifulSoup, pandas and jupyter. You can check them out if you want. 










