---
layout: default
title: 如何合并分割pdf文件
published: true
author: gro
comments: true
date: 2008-08-10 10:08:34
tags:
    - pdfsam
    - 分割pdf文件
    - 合并pdf文件
categories:
    - app
permalink: /2008/08/10/how-to-merge-split-pdf-files.html
---
有时候我们拿到的pdf文件很大, 但是我们只需要其中一部分内容. 或者我们想把几个单独的pdf文件组合在一起, 形成一个文件, 这样阅读, 保存, 共享都更加方便. 那么如何将pdf文件合并或分割开来呢, 下面介绍两个实现pdf文件合并分割功能的软件:

**PdfMerge**

我使用的是pdfmerge1.18版, 运行于Windows系统. 最新版可以到[主页下载][1], 下载后解压, 然后运行PdfMerge\bin\Release下面的PdfMerge.exe文件, 出现的程序主界面如下:

[][2]

使用的方法很简单, 点击Add Files按钮添加你想合并到一起的文件, 然后指定输出位置和文件名, 在点绿色的Merge按钮就可以了.pdfMerge还可以在命令行使用, 在解压的文件中readme中有相关说明, 这里就不介绍了.

在使用的过程中, 发现这款软件对中文pdf文件支持不好, 合并中文文件的时候就失去响应. 而且官方主页写着可以合并和分割文件, 但我没发现分割pdf的用法, readme中也没有. 所以, 下面再推荐另外一个同类的软件.

**pdfsam**

pdfsam也是开源软件, 最新版可以在[官方主页下载][3], 我使用的是pdfsam basic 1.0.0 stable版.

如果你下载的是zip包, 解压后双击pdfsam-1.0.0.jar运行程序(需要java runtime的支持, 如果发现系统没有java的环境, 到这里下载[Java Runtime Environment (JRE) 6 Update 7][4]应该就可以), 程序主界面如下:

[][5]

在左侧窗口中, 可以选择菜单导航, 合并分割文件, Settings等等, Settings里面可以设置界面语言(**包括简体中文**)和风格, 默认工作路径等.

**如何合并pdf文件**

首先, 选择Merge/Extract, 然后在右侧窗口中点Add可以加入要合并的pdf文件, 之后设置输出路径, 还要选择pdf的版本 &#8211; 默认的是Acrobat 6. 最后, 点击Run按钮, 很快就产生了合并后的文件.

在加入源pdf文件时, 窗口中会显示一些文件的信息, 比如文件路径, 页数, pdf的版本等, 你可以在Page Selection中指定哪几页需要合并, 指定文件的密码等等, 如下图:

[][6]

**如何分割pdf文件**

要分割文件也很简单, 点击左侧的Split, 点击右侧窗口中Add, 加入要分割的文件, 然后再options里面选择按什么方式分割. 常见方式有基于页码分割和按文件大小分割, 根据需求自己选择. 之后, 指定输出文件夹和文件前缀, 点Run, 在输出位置就会生成若干也前缀开头的文件.

这款软件有Windows和Mac的版本, 对中文支持很好, 我尝试分割合并了几个文件, 都没有问题, 而且界面语言可以设置为中文, 也很方便, 推荐使用.

更新:

在1.0.0版中按指定大小分割文件会有问题, 但按页码分割表现相当好, 等待今后版本的改进:)

更新2:

软件已经放出1.0.1 basic版, 之前按文件大小分割时出现的bug已经解决, 在这里下载. 补充说明, 按文件大小分割指定的大小只是大概数值, 分割出来的文件不会出现断页的现象.


  Technorati Tags: pdf merge,pdf split






 [1]: http://sourceforge.net/project/platformdownload.php?group_id=217208 "下载pdfMerge"
 [2]: http://getfreeware.net/wp-content/uploads/2008/08/pdfmerge-screenshot.png
 [3]: http://www.pdfsam.org/?page_id=32 "下载pdfsam"
 [4]: http://java.sun.com/javase/downloads/index.jsp "jre download"
 [5]: http://getfreeware.net/wp-content/uploads/2008/08/pdfsam-screenshot.png
 [6]: http://getfreeware.net/wp-content/uploads/2008/08/pdfsam-page-selection.png