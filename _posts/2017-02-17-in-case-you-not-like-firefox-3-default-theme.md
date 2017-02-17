---
layout: default
title: '假如你不喜欢Firefox 3的默认主题 [Firefox 3 Theme]'
published: true
author: gro
comments: true
date: 2008-06-24 10:06:18
tags:
    - Firefox
    - Firefox Theme
categories:
    - app
permalink: /2008/06/24/in-case-you-not-like-firefox-3-default-theme.html
---
Firefox 3没有保留经典的1.5版主题(皮肤), 而新换的主题不合我的胃口, 不好看, 很生硬. 费了半天劲, 终于让我找到了[旧版主题][1]. 安装以后, Firefox的外观就变成了2.0的样子, 这样用起来才顺手:D

下载: [Firefox 2 theme for Firefox 3][2]

作者在介绍中说做最好配合oldbar一起使用, 貌似就是之前介绍的那个[禁用AwesomeBar的插件][3]吧. 插件的评论绝大多数都给了5星, 有几个打分偏低的也是在抱怨为什么在Linux和OS X上不能用, 看来有人和我一样偏爱旧式界面.

顺带的说一下3版中的全屏, 比以前更彻底, 头部的地址栏, 标签栏会缩进去了, 终于不像以前那样不伦不类. 对于大显示器也许全屏不重要, 但使用笔记本和小显示器的时候还是能派上用场的.

如果出于某种原因你不喜欢现在的全屏方式, 那可以按下述方法修改之: 进入about:config, 在filter中输入browser.fullscreen.autohide, 双击将它的值设置为false.

另外, 将browser.fullscreen.animateUp的值设置为0, 可以关闭缩进时的动画效果.

 [1]: https://addons.mozilla.org/en-US/firefox/addon/6898
 [2]: https://addons.mozilla.org/en-US/firefox/downloads/file/31186/firefox_2_theme_for_firefox_3-0.8.19-fx.jar
 [3]: http://getfreeware.net/archives/388.html
