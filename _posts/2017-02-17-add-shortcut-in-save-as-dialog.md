---
layout: default
title: 在另存为…对话框中添加快捷方式
published: true
author: gro
comments: true
date: 2008-11-01 11:11:57
tags:
    - 另存为
categories:
    - app
permalink: /2008/11/01/add-shortcut-in-save-as-dialog.html
---
我现在基本上不使用Flashget等下载工具, 而是直接在浏览器中使用**右键-另存为…**的方式下载.

这个另存为对话框一般都会保存上次使用时保存文件的路径, 想保存到其他目录就要手动选择, 十分麻烦, 尤其时像我这样电脑运行多个程序, 资源紧张, 或者文件夹目录很深的时候, 打开那个目录下拉框往往需要一个让人难以忍受的等待时间.

默认情况下, 另存为对话框左侧有几个快捷方式, 包括桌面, 我的文档, 我的电脑等, 能不能在这里加入自定义的文件夹, 方便我们的操作呢?



下面就是解决方法:



1. 点击开始-运行, 输入**gpedit.msc**,打开组策略:



2. 然后在左侧的导航菜单中依次打开**User Configuration – Administrative Templates – Windows Components – Windows Explorer – Common Open File Dialog**, 中文系统可参照下图, 应该不难:



3. 这时, 双击右侧窗口中的一个**Items displayed in Places Bar**, 会出现如下设置窗口:



4. 选**Enable**, 然后在下面的5个输入框中添加你常用的文件夹的**完整路径**, 点击**应用** &#8211; **完成**即可.

5. 这时再试试另存为对话框, 看看左侧是不是已经变为你定义的快捷方式了:



PS, 不光再浏览器中, 在将文件(txt文件, Word文档等等)另存为的时候也一样.

PS2, 特意找了一个中文系统看了一下说明, 在设置窗口中(倒数第二张图片), 有一个说明页, 其中的内容是这样的:

> 配置 Windows 文件/打开对话框中的、“位置栏”中显示的项目列表。如果启用此设置，您可以在“位置栏”中指定显示 1-5 个项目。
> 
> 在“位置栏”中显示的有效项目为:
> 
> 1) 指向本地文件夹的快捷方式&#8211; (如，C:Windows)
> 
> 2) 指向远程文件夹的快捷方式 &#8212; (\servershare)
> 
> 3) 公共外壳文件夹。
> 
> 可以指定的常规外壳文件夹:
> 
> CommonDocuments, CommonMusic, CommonPictures, Desktop, MyComputer, MyDocuments, MyFavorites, MyMusic, MyNetworkPlaces, MyPictures, Printers, ProgramFiles, Recent。
> 
> 如果禁用或不配置此设置，这些项目的默认列表会显示在“位置栏”中。

从此我们可知:

  * 最多可以自定义5个常用路径
  * 可以定义本地文件夹, 网络文件夹, 或者是系统预定义(不知道这么说是不是准确)的外壳文件夹