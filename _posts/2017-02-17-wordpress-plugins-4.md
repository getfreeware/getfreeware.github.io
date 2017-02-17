---
layout: default
title: 'WordPress插件推荐 #4'
published: true
author: gro
comments: true
date: 2008-05-18 10:05:52
tags:
    - unused link category
    - WordPress-插件
categories:
    - app
permalink: /2008/05/18/wordpress-plugins-4.html
---
很多人都会在自己的blog中加一个联系表格, 这样不用暴露自己的邮件地址, 可以防止被垃圾邮件侵袭, 看起来也很酷很专业. 前面介绍过一个cforms II插件, 功能相当丰富, 除了可以实现简单的联系表格, 还可自定义生产其他种类的表格用于blog. 但我总觉得这插件过于庞大, 除了contact form, 其他的众多功能我都用不上, 甚至可以说是懒得非力气去研究 &#8211; 杀鸡焉用牛刀.

如果你和我一样, 只需要一个简单的contact form, 那可以试试看WP-Lightform插件. 他使用AJAX技术, 并且加入了防垃圾功能, 可以检查用户输入和自定义表格元素. 他基于LightForm, FormCheck和Niceforms三个插件, 你可以在这里看到演示: http://www.artflutter.com/beta/wp-lightform/



下载WP-Lightform: WP-LightForm _(version 0.2, 17-05-2008)_

**安装时注意:**

在解压后的文件中, 找到userinfo.php, 文件里允许你设置email, 可以是本文的作者email, 或者是你指定的一个email地址, 或者管理员(admin of blog)的email. 在三者中选一个, 并将其他两个加上注释(//).

**使用中遇到的错位问题及解决方法:**

安装以后, 发现该插件在默认模板中可以正常显示, 但是在另外一些模板中显示异常. 如图:



造成这种错位效果的原因是某些wordpress主题的css文件定义了文章中img标签的属性, 比如margin, border, padding等等. 解决办法是在插件目录下编辑这个文件: csslightform.css. 在文件的末尾添加如下代码:

> #lightform img {
  
> float: none;
  
> margin: 0px;
  
> border: 0px solid white;
  
> padding: 0px;
  
> }

**链接及相关阅读:**

WP-LightForm下载 (version 0.2, 17-05-2008)

cforms II和中文翻译

WP-LightForm发布页面

update:

Gxgz对这个插件做了汉化, 在这里下载:WP-LightForm 简体中文版

感谢!