---
layout: default
title: 安装好WordPress之后需要做的一些事情
published: true
author: gro
comments: true
date: 2008-03-24 09:03:00
tags:
    - unused link category
categories:
    - app
permalink: /2008/03/24/things-after-installing-wordpress.html
---
[][1]

安装Wordpress并不复杂, 对于很多独立blogger来说可以说是轻而易举. 需要注意的是, 在开始发表文章之前, 应该再调整一些配置, 做一些优化. 这样做既可以加快站点的推广速度, 又可以省掉很多麻烦(比如垃圾留言, 或者是更换feed地址带来的流量损失等).

Jason Blanton的文章就总结了以下5点:

  1. **改变固定链接**:
  
    Wordpress默认的permalink结构是: http://www.yourdomain.com/?p=21, 但这样的结构更利于SEO: http://www.yourdomain.com/the\_next\_great_article . 但老外总结的不太适合中文blogger, 关于固定链接, 还可以参考这篇文章: http://www.williamlong.info/archives/1027.html .
  2. **换一个主题**:
  
    一款好的主题会凸显内容, 让人印象深刻, 选一款好的主题, 从这里开始: http://themes.wordpress.net/ .
  
    我也总结过几款免费的杂志型的主题, 原文地址: http://getfreeware.net/?p=33 .
  3. **添加ping服务**:
  
    更新服务可以显示你blog的更新. 每次你发表文章的时候, WordPress都会自动发送一个XMLRPC ping到提供更新服务的网站. 这里列出了一些国外常见的ping服务器地址, 国内也有, 比如: http://www.feedsky.com/ping.html . 如果不想每次手动ping这些服务器的话, 就把RPC地址填到Options-Writing里的Update Services里.
  4. **激活akismet插件**:
  
    这是Wordpress自带安装的防垃圾评论插件, 尽可能早的激活吧.
  5. **用FeedBurner烧录你的feed**:
  
    网上关于FeedBurner的相关文章很多, 国内提供类似服务的是刚刚提过的Feedsky.

这5点总结的很基本. 我倒是觉得很多事情应该在开始安装Wordpress之前就考虑清楚, 比如:

  1. 用什么样的固定链接格式 &#8211; 频繁的更换固定链接结构会损失流量, 不利于培养固定用户群.
  2. 到底是用feed托管(烧录)还是用自带的feed输出? &#8211; 你真的相信托管服务吗, 要知道国外的网站动不动就无法连接, 而国内的服务质量和稳定性也让人担忧.

其实每个blogger都有自己的需求, 具体设置因人而异. 这里就依然使用默认的permalink结构, 虽然烧了feed, 但目前没有公开使用的打算. 我觉得以上5点, 只有激活akismet插件最为迫切. 网站宣传, SEO等等辅助手段, 也总是要建立在内容的基础上.

 [1]: http://getfreeware.net/wp-content/uploads/2008/03/wp-logo.jpg