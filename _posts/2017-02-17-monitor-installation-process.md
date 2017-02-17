---
layout: default
title: 监视软件安装过程中的后台操作
published: true
author: gro
comments: true
date: 2008-04-13 06:04:52
tags: [ ]
categories:
    - app
permalink: /2008/04/13/monitor-installation-process.html
---
软件安装过程时一般会对注册表做修改, 同时还会在系统中创建一些目录和文件, 有些软件还需要联网检查程序更新, 获取最新的文件. 这整个过程中的大部分操作是在系统后台进行的, 用户并不可见. 这种不透明让人很担心, 如果软件来自人们普遍信任的公司或许还好, 但是面对互联网上层出不穷的软件, 和关于很多软件的负面新闻, 我们还能相信软件的安装过程不会给系统带来垃圾, 留下隐患吗? 下面这几个免费的小程序在某种程度上可以让我们更清楚明白软件到底在&#8221;安装&#8221;什么, 如果你和我一样担心(或者是好奇)的话, 可以尝试使用[via Digital Inspiration].

  1. Regshot
  
    这个91k大小的小工具可以记录程序安装前后注册表的变化, 并输出纯文本或HTML格式的报告.只要在安装程序前后分别做一个注册表的&#8221;截图&#8221;(1st shot 和 2nd shot)就可以了.
  
    
  2. ProcMon
  
    这是微软提供的一个小工具. 它可以实时监视文件系统, 注册表以及进程/线程的任何活动. 利用它, 你可以了解程序都接触了哪些文件和文件夹.
  
    
  3. URL Snooper
  
    这个工具更类似于一个网络监视器. 很多程序都有检查更新的功能, 你只要打开URL Snooper, 点击&#8221;Sniff Network&#8221;, 然后在开始进行检查更新, 就可以知道程序下载的路径/URL. PS, 浏览URL Snooper主页的时候发现, 这个小程序其实是用来过滤获取音频和视频文件地址的.
  
    