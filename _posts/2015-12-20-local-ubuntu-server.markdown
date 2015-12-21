---
layout: post
title:  "Running a local Ubuntu server"
date:   2015-12-20
categories: devops
permalink: /local-ubuntu-server
---
{% include stupid.html %}

## Why should you run a local Ubuntu Server?

It's becoming more and more common to heavily rely on cloud computing when it comes to creating development environments of any kind. That is the future of development without any doubt. However, I like to be able to run my dev server locally. There are several reasons. It's educational, saves money and makes you less dependent on an Internet connection while developing.

###Running an Ubuntu server on a mac

 - I am going to use ORACLE's free [VirtualBox](https://www.virtualbox.org/wiki/Downloads) to host my Ubuntu server.
 - [Download](http://www.ubuntu.com/download/server) desired version of Ubuntu server.
 - Create new virtual machine.
    - Under storage, point to .iso file.
    - Network > Select bridge adaptor.
    - Only select OPENSSH and use defaults.
 - Start server in VirtualBox.
 - Log into server.
 - Update and upgrade.
 - Run `ifconfig` to find your ip address
 - Open your terminal and run `ssh username@ip`
 - `sudo tasksel` lets you select from a large list of available add-ons.


{% include disqus.html %}
