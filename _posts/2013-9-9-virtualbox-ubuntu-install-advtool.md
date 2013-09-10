---
layout: post
title: "在VirtualBox中安装Ubuntu 的增强工具包"
tagline: "在VirtualBox中安装Ubuntu 的增强工具包"
description: "在VirtualBox中安装Ubuntu 的增强工具包"
tags: [normal]
---
{% include JB/setup %}

1. **安装编译环境**，执行如下命令


    sudo apt-get install build-essential

2. 进入`cd /media/cdrom`
3. 执行 `sudo ./VBoxLinuxAdditions-x86.run`
4. 完成后重启 
