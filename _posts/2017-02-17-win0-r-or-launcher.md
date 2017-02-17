---
layout: default
title: 用Win+R还是用Launcher?
published: true
author: gro
comments: true
date: 2008-08-24 05:08:00
tags: [ ]
categories:
    - app
permalink: /2008/08/24/win0-r-or-launcher.html
---
**关于Launcher**

以前用过几个Launcher程序, 但过不了多久就都卸载了. 说不上不喜欢, 但总觉得一个程序占那么多内存, 也没给操作带来多大效率上的提高, 有点鸡肋. 可能这些程序外观很吸引人, 也提供了一些实用的功能, 但长久以来形成的电脑使用习惯, 并不那么容易改变.

**快速启动栏**

快速启动程序的方法很多, 最最最简单的是在桌面上放快捷方式. 但如果桌面上放了太多的图标, 眼花缭乱, 也很不方便. 另外, 每次都要最小化所有的窗口, 才能看见桌面, 大大影响了工作效率. 后来, 所有的快捷方式都被我放到了快速启动栏里, 这样在任务栏的左侧就罗列了一大排快捷方式.

**Win+R快速启动程序**

这样已经很顺手, 但我们还可以继续捣鼓一下, 实现Win+R快速启动常用程序.



首先, 在电脑中创建一个文件夹, 比如&#8221;E:\shortcurs&#8221;, 然后把所有的快捷方式都放到这个文件夹里面. 可以根据自己的习惯和喜好重命名这些快捷方式, 之后我们要用这些名字当作命令直接启动程序, 比如, 我把Firefox 2改为ff2, 画笔改名为pt.

然后, 在系统变量中加入这个文件夹的路径, 具体做法是: 右键点击我的电脑-属性-高级-环境变量, 在下面的系统变量窗口中找到path, 点编辑按钮, 在变量值里末尾加入分号&#8221;;&#8221;和刚刚创建的文件夹路径&#8221;E:\shortcuts&#8221;, 然后确定.

这时, 我们按Win+R调出运行窗口后, 输入ff2就可以直接启动Firefox 2, 而pt自然与画笔相对应了. 在运行对话框中还可以直接输入网址, 文档, 或文件夹等资源来快速启动相关联的程序.

下面是几个常见的Launcher软件, 看不上Win+R的同学不要错过:

[Launchy][1] &#8211; 开源的键盘快速启动程序(Windows)

[Executor][2] &#8211; 多功能的程序启动器(Windows)

[Speed Launch][3] &#8211; 微软公司的同类软件

[Gnome Do][4] &#8211; Dont Search, Do!(Linux)

补充:

经HansonDon推荐,补充收录一个Windows悬浮命令行小工具 &#8211; SlickRun. 根据主页介绍, SlickRun可以给常用的程序创建别名, 这样, 直接输入简短的别名, 就可以执行相关联的程序. 

一个人力量有限, 希望熟悉其他同类软件的朋友留言推荐补充, 再次感谢HansonDon :)


  Technorati Tags: Win R,Launcher


 [1]: http://www.launchy.net/ "Launchy主页"
 [2]: http://executor.dk/ "Executor 主页"
 [3]: http://www.officelabs.com/projects/speedlaunch/Pages/default.aspx "Speed Launch 主页"
 [4]: http://do.davebsd.com/ "Gnome Do 主页"