---
layout: default
title: >
    Smart Location Bar – Firefox 3.0
    地址栏的新功能介绍
published: true
author: gro
comments: true
date: 2008-06-21 10:06:24
tags:
    - Firefox
categories:
    - app
permalink: /2008/06/21/smart-location-bar-firefox-3-0.html
---
相比于之前的版本, Firefox 3.0的地址栏有了很大的改动, 增加一些功能, 它也进而被称为Smart Location Bar 或者AwesomeBar. 本文下面的内容是关于这个新功能的介绍, 以及如何禁用这个功能(如果你更习惯于Firefox 2.0地址栏的话).

**Smart Location Bar (Firefox 3.0)**

当你在地址栏开始输入文字的时候, Firefox会根据你曾经访问过的网页自动生成一个下拉列表. 列表中包括与输入文字所匹配的网址信息, 网站的favicon等等. 听起来和以前的地址栏区别不大, 还是看图说话吧(来自[Firefox Support][1]):



如上图所示, 输入aw后, Firefox根据历史记录, 收藏夹等记录, 产生了一个网址列表, 并且与&#8221;aw&#8221;匹配的地方加粗显示. 网页的标题, 网址, 甚至网页的标签都在查找范围内. 再看下图(来自[Firefox Support][2]):



不仅如此, 还可输入多个关键词, 以空格分隔. Firefox会自动匹配同时包含这些关键字的网页, 如下图所示(来自[Firefox Support][3]), 输入s和m两个字母, 会出现如Safe Mode这样的记录:



这些记录匹配自浏览器的历史记录, 收藏夹, 和收藏夹中的标签, 所以如果你愿意使用这个新功能, 最好保留一定的历史记录, 在收藏夹中加注tag也会提高匹配的精度.

**禁用Smart Location Bar/Awesome Bar (Firefox 3.0)**

并不是每个人都喜欢这项功能, 我就觉得他多此一举, 占据空间, 而且过多的粗体匹配关键字看起来很乱, 暂时还是习惯于旧式的地址栏. 如果你也想这么做, 那最简单的方法是安装[oldbar][4]这个扩展, 它会将Firefox 3.0地址栏恢复到2.0的样子.

如果只是想调整一下Smart Location Bar的条目, 可以在about:config中找到[browser.urlbar.maxRichResults][5]一项, 他的数值代表出现在下拉列表中条目的最大数量, 默认值12. 如果设为-1, 那将不产生下拉列表.

 [1]: http://support.mozilla.com/en-US/kb/img/wiki_up/awesomebar_window.png "Firefox awesome bar"
 [2]: http://support.mozilla.com/en-US/kb/img/wiki_up/awesomebar_examples4-crop.png "Firefox awesome bar demo"
 [3]: http://support.mozilla.com/en-US/kb/img/wiki_up/awesomebar_non_word_match.png "Firefox awesome bar example"
 [4]: https://addons.mozilla.org/en-US/firefox/addon/6227 "Firefox extension oldbar"
 [5]: http://kb.mozillazine.org/Browser.urlbar.maxRichResults "Firefox about:config browser.urlbar.maxRichResults"