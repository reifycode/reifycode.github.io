---
layout: post
published: true
exacttime: "10:57:00"
title: "Using Nmap for Your Own Security"
category:
- "ubuntu"
- "security"
headimg_url: "/images/ubuntu/ubuntu.jpg"
author: thepulkitagarwal
---

Nmap (or Network Mapper) is a security scanner, that is used to discover hosts and services on a computer network. This means that you can use it to discover open ports on your own computer, or someone else's computer which is on your network.

Open ports on your computer are a major security concern - they are one of the most used ways to gain access to your computer. In fact, the only way your computer can connect to the outside world (read: the internet) is through an open port.

You can check the open ports on your computer by first installing nmap, and then running: `nmap localhost`

Recently I installed something on Ubuntu, and that just happened to open a couple of random ports. As I didn't require it as such, I used the command:

`sudo service nameOfService stop` 

for each of the services, with the correct name instead of 'nameOfService'. But, as I found out later, this was only a temporary solution. A quick Google search showed that I needed to modify some config file so that it didn't start again on boot. This was the command I used:

`sudo update-rc.d -f nameOfService remove`

I thought this would work fine. And it does work fine for a lot of services. But for many others (like MySQL), this doesn't work properly. Using [this answer from the Ask Ubuntu Forums](https://askubuntu.com/questions/40072/how-to-stop-apache2-mysql-from-starting-automatically-as-computer-starts/40077#40077) as reference, I did:

`sudo echo "manual" >> /etc/init/nameOfService.override`

This command is used to stop Upstart from automatically starting something. Upstart is something that basically starts and stops tasks and services in Ubuntu. Read more about [the section "Disabling a Job from Automatically Starting" in the Upstart Cookbook](http://upstart.ubuntu.com/cookbook/#disabling-a-job-from-automatically-starting).

In case you get a bash permissions error in the last step, try the following:

`cd /etc/init/`
`sudo gedit nameOfService.override`

And in the gedit text editor that opens, type "manual" (without the quotes), and save. You can use any text editor that you want instead (like subl for sublime text and so on).