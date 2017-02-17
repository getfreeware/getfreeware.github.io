---
layout: default
title: >
    如何使用del.icio.us的daily blog posting功能(for
    WordPress)
published: true
author: gro
comments: true
date: 2008-03-16 08:03:47
tags:
    - unused link category
categories:
    - app
permalink: /2008/03/16/delicious-daily-blog-posting-for-wordpress.html
---
http://del.icio.us就是那个所谓的美味书签, 可以把自己感兴趣的文章/网站链接收集起来. del.icio.us有一个叫做&#8221;daily blog posting&#8221;的功能, 可以将你每天添加的链接做一个列表, 自动发送到你的blog上. 在del.icio.us的设置页面里, 他号称支持:Movable Type, Typepad, WordPress, 以及其他blog平台.(我想应该需要blog系统有XML-RPC接口)

这里用的是wordpress, 简单记录一下配置的过程:

1. 登录del.icio.us后, 点右上角的settings, 然后点Blogging下面的daily blog posting进入配置页面

2.点击页面中部的add a new thingy, 之后的各项含义如下:

**job_name:** 这个&#8221;thingy&#8221;的名字, 随便填写即可, 比如&#8221;感兴趣的文章&#8221;
  
**out_name:** wordpress用户名
  
**out_pass:** 该用户名的登录密码(**密码会明文显示, 所以建议新创建一个用户而不是管理员, 新用户的role设置成Editor即可.**)
  
**out_url:** XML-RPC接口的地址, 对于wordpress来说, 应该是http://你的域名/xmlrpc.php
  
**out_time:** 每天自动送链接的时间(用GMT 0-23 表示), 我写的是0
  
**out\_blog\_id:** blog的ID号(如果只有一个blog就写1吧)
  
**out\_cat\_id:** 发送的文章所属的分类. 需要到wordpress的后台去确定分类的id.(**如果这项可以不填, 应该会归到默认的分类**)

3. 填好以后点Submit Query即可.

不知道今后这个功能会如何改进, 如果可以在加入自动发文的标题设置就更好了.

其实网上的书签服务很多, 如果不喜欢E文, 也可以选择国内的服务, 可以参考国内国外网摘站点这篇文章.

另,
  
其实这种网摘/书签真的那么有用吗?
  
我保存过的网页很少再去浏览, 查找资料每次都是google或者baidu.
  
浏览器自带的书签其实更快更方便, 再加上google toolbar, 共享同步的问题也可以解决.
  
也许网摘对于网站的宣传还是有一定作用的, 前提是网站的内容被大家认可.
  
过几天会取消这个自动发帖, 搞的页面很乱.