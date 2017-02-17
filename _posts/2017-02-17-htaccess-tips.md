---
layout: default
title: Htaccess 设置小技巧
published: true
author: gro
comments: true
date: 2008-03-17 09:03:44
tags:
    - Linux
categories:
    - app
permalink: /2008/03/17/htaccess-tips.html
---
前面写了一篇用htaccess防止图片盗链的文章, 这次再总结一些htaccess文件的其他用处:

  * 设置时区

> SetEnv TZ America/Chicago
> 
> 时区的列表可以在这里找到: http://us2.php.net/manual/en/timezones.php

  * 链接扩展名 &#8211; Different File Extension

> Options +FollowSymlinks
  
> RewriteEngine on
  
> RewriteRule ^(.*).zig$ $1.php [nc]
> 
> 这样, 访问example.zig就相当于example.php

  * 取消扩展名

> Options +FollowSymlinks
  
> RewriteEngine On
  
> RewriteCond %{REQUEST_FILENAME} !-f
  
> RewriteCond %{REQUEST_FILENAME} !-d
  
> RewriteRule ^(.*)$ $1.php [L,QSA]
> 
> 这样做以后, 网址URL中不会显示.php这个后缀

  * 拒绝访问包含文件 &#8211; Deny Access to Include Files

> 
  
> Order allow,deny
  
> Deny from all
  
> 
> 
> 阻止其他人浏览inc文件, 有点疑惑, 貌似是禁止访问inc文件夹中的所有文件.

  * 拒绝文件夹列表

> Options -Indexes 
> 
> 如果文件夹中没有index文件的话, 这个设置会拒绝其他人浏览文件夹的内容.

  * 404转向, 重定向

> ErrorDocument 404  
> 
> 很明显, 将404错误页面设置(转到)为http://exmple.com/ (原文如此, 明显是把example错误拼写为exmple了)

  * 加快网页加载时间

> 
  
> mod\_gzip\_on Yes
  
> mod\_gzip\_dechunk Yes
  
> mod\_gzip\_item_include file .(html?|txt|css|js|php|pl|jpg|png|gif)$
  
> mod\_gzip\_item_include handler ^cgi-script$
  
> mod\_gzip\_item_include mime ^text/.*
  
> mod\_gzip\_item_include mime ^application/x-javascript.*
  
> mod\_gzip\_item_exclude mime ^image/.*
  
> mod\_gzip\_item_exclude rspheader ^Content-Encoding:.\*gzip.\*
  
> 
> 
> 需要有mod_czip.c模块的支持, 可以将传输的内容压缩55-65%, 从而提高35-40%的速度(当然都是理想状态)

  * 显示站点维护状态页面

> Options +FollowSymlinks
  
> RewriteEngine on
  
> RewriteCond %{REQUEST_URI} !/maintenance.html$
  
> RewriteRule $ /maintenance.html [R=302,L]
> 
> 用上述命令, 网站浏览者将会被带到maintenance.html这个页面, 在维护网站的时候很有用.

翻译的并不是很准确, 所以附上了部分英文, 这些小技巧来全部翻译自dreamhost的wiki. 互联网上还有其他的资源可以参考, 推荐以下两篇:

中文: [http://hellobmw.com/archives/using-htaccess.html][1]
  
英文: [http://www.freewebmasterhelp.com/tutorials/htaccess/1][2]

 [1]: http://hellobmw.com/archives/using-htaccess.html "http://hellobmw.com/archives/using-htaccess.html"
 [2]: http://www.freewebmasterhelp.com/tutorials/htaccess/1 "http://www.freewebmasterhelp.com/tutorials/htaccess/1"