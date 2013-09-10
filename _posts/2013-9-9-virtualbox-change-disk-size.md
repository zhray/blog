---
layout: post
title: "SSH Public Key登录"
tagline: "SSH Public Key登录"
description: "SSH Public Key登录"
tags: [normal]
---
{% include JB/setup %}

进入virtualbox的目录，在命令行下输入如下命令

	# 列出磁盘，找出要修改大小的磁盘的uuid
    VBoxManage list hdds
	# 修改磁盘大小为40G，40960=40G
    VBoxManage modifyhd uuid --resize 40960

**备注：***40960=40G*