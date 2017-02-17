---
layout: default
title: U盘写保护工具
published: true
author: gro
comments: true
date: 2008-11-26 10:11:09
tags:
    - U-drive
categories:
    - app
permalink: /2008/11/26/make-u-drive-write-protected.html
---
有些U盘上自带一个开关, 可以控制U盘是否只读. 但大多数人正在用的U盘没有这个功能. 我们可以用一些软件来实现U盘写保护的功能.

**Thumbscrew**

 下载Thumbscrew, 解压以后, 运行thumbscrew.exe, 就会在系统托盘中出现一个图标. 右键点击这个图标, 选择Make USB Read Only, 然后在插入U盘, 这时你的U盘就会变成只读状态, 这时系统托盘中的图标会变成红色禁止符号. 要改回可写入状态, 右键点击图标, 选择Make USB Writable即可.

**USB WriteProtector**

USB WriteProtector也实现类似的功能, 但是界面不同, 而且支持多语言(支持繁体中文, 但在我系统上显示乱码, 还不如用e文).



如图, 选择USB write protection ON, 然后点Close, 再重新插入U盘, U盘就变成写保护状态了. 选择USB write protection OFF再重新插入U盘, 即可正常读写.

**缺点**

用软件实现U盘的写保护其实作用不大, 只有在安装了该软件的电脑上才起作用, 并不能成为U盘自身的功能; 而且更改状态需要重新插入U盘一次才可以实现. 有没有什么软件能在U盘上做些改变, 使它在每台机器上使用的时候都是写保护状态的呢?

**优点**

两款软件都很小巧, 使用不需要安装, 使用直接解压运行即可.

网吧, 机房等地的电脑上可以选择安装并默认运行这种软件进行U盘写保护, 由用户选择是否需要打开U盘的可写状态, 可以在一定程度上减少U盘病毒的传播. 上次我就是用了一个从实验室机房拿回来的U盘不小心中招, 所幸不是恶意病毒, 但是卡巴斯基竟然没有发现.