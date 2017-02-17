---
layout: default
title: Ultimate Defrag – 整理磁盘碎片, 提高系统性能
published: true
author: gro
comments: true
date: 2008-05-24 08:05:20
tags:
    - Ultimate Defrag
categories:
    - app
permalink: /2008/05/24/ultimate-defrag-disk-defragment-tool.html
---
使用电脑时间长了, 硬盘的空闲扇区会分布在不连续的物理位置上, 这样文件数据就不能存在连续的物理地址上. 在读取硬盘上的数据是, 硬盘的磁头就需要反复移动, 影响了速度, 降低了整个系统的性能. 为了充分发挥硬件性能, 我们应该定期整理磁盘碎片. 这样, 物理上数据会被集中到连续的扇区, 必然增加文件读取的速度.

Windows自带了磁盘碎片整理工具, 位置在: 开始-程序-附件-系统工具-磁盘碎片整理工具. 打开这个工具以后, 你可以看到每个分区的状态. 要进行磁盘整理, 每个磁盘必须有至少15%的空闲空间. 你可以先点分析按钮, 这样, 程序会对驱动器进行扫描分析, 结束后会提示你是否需要进行碎片整理.

说了半天, 还没进入主题, 今天要介绍的是一个第三方的免费磁盘碎片整理软件 &#8211; Ultimate Defrag. 它的与众不同之处在于可以根据个人需要, 把数据放到性能表现不同物理位置 &#8211; 硬盘越靠外访问越快(?).

运行程序以后, 右侧显示了硬盘的图像, 左侧是不同的驱动器和若干选项.

[][1]

左侧提供的整理方法大致翻译如下:

  * Fragmented Files Only: 整理磁盘, 和Windows的整理工具类似.
  * Consolidate: 将所有文件夹连续存放, 以减少寻访时间.
  * Folder / File Name: 按文件夹名称排列.
  * Recency: 针对于存贮数据的驱动器. 按最后访问时间, 最后修改时间和创建时间排序.
  * Volatile: 按最后修改时间和名称排序.
  * Auto: 自动, 使用程序自带的优化算法进行整理.

**UltimateDefrag 下载: 地址1 | 地址2 | 地址3 |**
  
版本: 1.72 (23 May 2008)
  
系统要求: Windows XP/ Vista

source: gHacks

 [1]: http://getfreeware.net/wp-content/uploads/2008/05/ultimate-defrag-500x388.jpg