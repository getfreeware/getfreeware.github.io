---
layout: default
title: goosh.org – 命令化google搜索
published: true
author: gro
comments: true
date: 2008-06-26 10:06:09
tags:
    - Google
    - Webware
    - 谷歌
categories:
    - app
permalink: /2008/06/26/goosh-org-command-line-google.html
---
发现一个很有意思的网站 &#8211; [goosh.org][1]. 它利用google提供的API, 将搜索做成了仿Unix Shell的命令行模样.

打开网址后, 可以输入help或者h查看命令列表, 如下图:



其中绿色的命令指明了搜索的模式, 也就是说要搜索网页, 图片, 新闻资讯等等. 如果直接输入那些绿色的命令, 不带任何参数, 就会进入相应的模式中.

只要输入命令+关键字, 再按回车, 就可以返回搜索结果了. 默认的模式是web, 所以如果你直接输入关键字, 再按回车, 就会返回在网页中的搜索结果.

它还支持指定域名搜索: site 关键字, 以及其他一些非搜索类命令, 比如打开网页: go + url, 命令列表: ls, 登入登出google帐号: login/logout, 还有阅读撰写google邮件的功能: gmail.

下图是搜索结果的模样:



 [1]: http://goosh.org/