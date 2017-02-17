---
layout: default
title: '[推荐] ClipPath – 快速复制文件的完整路径'
published: true
author: gro
comments: true
date: 2008-05-27 09:05:11
tags: [ ]
categories:
    - app
permalink: /2008/05/27/clippath-copy-file-full-path.html
---
通常情况下, 如果我需要把文件的完整路径告诉给别人, 我会这样做:

1. 在Windows Explorer中找到这个文件   
2. 复制文件的名字   
3. 加到Address栏显示的路径的后面   
4. 再复制这个包含文件名的路径, 然后发给别人

虽然可以用F2, Home, End等按键加速整个过程, 但如果重复这个动作还是很麻烦. 而且, 你还要更改Windows Explorer的默认设置, 确保它显示完整路径和文件的扩展名.

除了上面的情况, 另外一种情况也很头疼.

开发软件的时候, 经常需要在程序中打开文件. 但在open对话框中层层寻找目标文件却大大减缓了速度, 降低了效率. 如果我之前已经复制了文件的完整路径, 就方便了, 可以直接粘贴在文件名一栏, 然后回车打开文件.

废了半天话, 其实要说是 &#8211; **我需要一个快速的方法来得到被选中文件的完整路径**. 如果正好你(通常应该是类程序员人群)也有这方面的需求, 就试试下面这个免费的小程序吧.

ClipPath, 一个Windows shell扩展程序. 安装以后, 可以让你快速方便的复制文件/文件夹的绝对路径到剪贴板. 他在Windows Explorer的右键菜单中添加新的项目来完成该功能, 如下图所示:

 

目前的版本, 可以生成Windows格式的路径(backward slash &#8221; 分隔), Unix系统格式的路径(forward slash &#8216;/&#8217; 分隔), 以及在outlook中使用的链接, 并随之复制到剪贴板中.

我将它归在开发工具中, 有了它, 真的是事半功倍啊:D


  
    ClipPath
  
  
  
    
      Version: 2.1
    
    
      环境: Win95/98/Me/NT4.0/2000/XP
    
    
      下载: Easy-Share | MediaFire |
    
  


安装:

下载以后, 解开压缩包, 右键点击ClipPath.inf文件, 选择安装(install)即可.

卸载:

在控制面板的添加删除程序中卸载, 然后重启电脑即可.

你可能注意到, 这款程序不支持Vista. 不要担心, 因为在Windows Vista中, 已经内置了类似功能, 只要你按住Shift, 然后右键点击选中的文件, 菜单中就会出现"Copy as Path"这个选项了:)