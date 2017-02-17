---
layout: default
title: 为什么WordPress2.6预览主题显示空白页
published: true
author: gro
comments: true
date: 2008-07-27 06:07:48
tags:
    - unused link category
categories:
    - app
permalink: /2008/07/27/why-wordpress-2-6-show-blank-page.html
---
在本地升级到2.6, 想看看对批量编辑功能有没有增强, 结果一如既往的失望. 正好在修改主题, 就顺便试试修改过的主题在2.6能不能正常显示, 结果发现2.6版预览主题时候总是显示空白, 但是可以选择激活主题, 而且激活以后, 主题显示, 功能都还正常.

搜了一下, 发现有人说一些插件和这个预览功能[有冲突][1], 已知的插件包括: Bowob chat and Stray Random Quotes. 但是我没装这两个插件, 索性一个个把所有插件都禁用, 但结果还是一样.

这时候发现, 我安装的6,7个主题, 只有一个出现这个情况, 预览其他几个的时候, 都正常. 于是想, 大概是这个主题有些与众不同的地方. 长话短说吧, 最终发现, 主题文件夹中包含&#8221;.&#8221;(点)的时候, 就会产生这种blank页的问题. 比如, 把&#8221;default&#8221;改为&#8221;defau.lt&#8221;.

接着又到[trac][2]上搜索了一下, 发现有个ticket很类似, 但他的情况是文件夹名字包含&#8221;-&#8220;或者&#8221;_&#8221;, 而且已经被解了. 那我就在[报一个好了][3], 呵呵.

不是什么很严重的问题, 但我习惯修改主题时用类似v1.1来命名文件夹, 没记得官网说过主题文件夹命名的问题啊&#8230;


  Technorati Tags: WordPress bug


 [1]: http://maketecheasier.com/wordpress-26-theme-changing-issue/2008/07/26 "plugin conflict with theme preview"
 [2]: http://trac.wordpress.org/ "trac - WordPress bug tracing system"
 [3]: http://trac.wordpress.org/ticket/7417 "Theme preview fails when Theme forlder contain dot"