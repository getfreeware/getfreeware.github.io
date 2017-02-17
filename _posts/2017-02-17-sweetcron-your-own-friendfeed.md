---
layout: default
title: SweetCron – 在自己的服务器上安装”FriendFeed”
published: true
author: gro
comments: true
date: 2008-09-07 11:09:30
tags:
    - Webware
categories:
    - app
permalink: /2008/09/07/sweetcron-your-own-friendfeed.html
---
你有自己的域名吗? 有自己的服务器或者是&#8230;虚拟主机吗? 你喜欢FriendFeed吗?

想不想把&#8221;FriendFeed&#8221;装到自己的服务器上, 然后以自己的域名访问之, 并介绍给好友呢?

好, 我承认我有点标题党了, 不过别急, 虽然我不能真的把FriendFeed安装在自己的服务器上, 但我有个更好的东西&#8230;起码是一样好的东西推荐给你 &#8211; SweetCron.

**1. 关于SweetCron**

用这套程序, 你可以非常轻松的聚合多种Web2.0的服务, 并以各种形式将之组合在一起, 呈现给访问者. 如果你没听明白, 可能你还没用过FriendFeed? 那可以先看看本站的FriendFeed页面 &#8211; [http://friendfeed.com/getfreeware][1].

看到了什么? 我在blog上发表的文章, 在delicious上添加的书签, 在Flickr上传的照片, 在Twitter上的消息等等等等, 各种各样的动作都会在FriendFeed上留下印记, 像一个流水帐的记录. 虽然我个人对此并不很着迷, 但我并不排斥它, 而且我觉得用这种服务做一个个人门户很不错, 朋友间交流也很好. 言归正传, 还是说说SweetCron吧.

首先, 先来看看我刚装好的SweetCron站点 &#8211; [http://i.getfreeware.net/][2], 是不是看上去很像FriendFeed呢? 在这里你会看到免费软件资讯站新文章, 我的美味书签中的新书签和我的Flickr上的照片, 并且每当有更新的时候, 都会**自动地**在这里出现.

可能看上去网站的样子比较简朴, 但实际上SweetCron是支持Theme和插件功能的(和WordPress一样), 只是我还没找到更喜欢的主题.

**2. 安装SweetCron**

英文的安装文档在这里: [http://code.google.com/p/sweetcron/wiki/Installation][3]. 下面简单翻译并说明一下:

1) 需求: 支持PHP5和MySQL4.1的服务器, 支持mod_rewrite模块, 一些你使用的网络服务的rss feed(比如blog的rss输出, Flickr的rss输出)

2) 创建一个新的数据库, 后面会用到

3) 将下载解压后的sweetcron文件夹里面的内容上传到服务器根目录, 这里假设你要在根目录安装. 然后再根目录下创建编辑.htaccess文件:

> Options +FollowSymLinks
  
> RewriteEngine On
> 
> RewriteBase /
> 
> RewriteCond %{REQUEST_FILENAME} !-f
  
> RewriteCond %{REQUEST_FILENAME} !-d
  
> RewriteRule ^(.*)$ index.php?/$1 [L]

然后做一些设置:

a. 在system/application/config/文件夹中, 将config-sample.php改名为config.php, 编辑这个文件, 将其中[http://www.your-site.com/][4]替换为你站点的URL, 包括斜杠末尾的/, 如图:

[][5]

b.在上述文件夹中, 将database-sample.php 改名为 database.php, 并修改其中的数据库服务器, 数据库, 用户名和密码部分, 如图.

[][6]

好, 保存这两个文件, 在浏览器中打开你的URL, 按照说明, 点击按钮安装就可以了. 需要注意的是, 如果是在子目录安装, 有两个地方要调整: 在config.php中, base_url应该是完整的url路径, 包含子目录, .htaccess文件中RewriteBase /改为RewriteBase /.

**3. 使用Sweetcron**

装好以后, 在如下地址登录后台: . 后台主要有5个标签页, 控制台显示最新的5个条目; 撰写(write)可以写一篇文章, 类似blog里面的post;Items里面编辑修改已经引入的, 自己撰写的文章条目等;Feeds一项可以配置需要自动聚合的源, 比如Flickr, 书签, blog等等;Options是对Sweetcron做一些设置的地方.关于更细节的地方, 以后慢慢来叙述吧.

**4. 相关链接**

和WordPress一样, 这个也是开源产品, 可以在这里下载:

[http://code.google.com/p/sweetcron/downloads/list][7]

我安装的是108b版, 在写这篇文章的时候, 108c版已经放出来了.当然现在还是beta版, 有些地方不稳定, 使用不方便也在所难免, 英文的文档在这里, 包括安装说明, API等等:

[http://code.google.com/p/sweetcron/w/list][8]

还有一个讨论组: [http://groups.google.com/group/sweetcron/topics][9]

作者Yongfook自己的个人站点就是用Sweetcron搭建, 大家可以看看, 使用的主题是源代码附带的boxy\_but\_good, 但我使用的时候发现, 导入blog的文章时, 图片会成文单独的item, 导致页面布局变得很难看, 所以现在暂时用sandbox这个主题.

在Yongfook的主页上, 他戏言Blog已死, 其实他的意思是blog已经不足以表现消费者的完整需求, Sweetcron这样的lifesteam会更流行. 没错, 不管是Blog, Flickr, 书签, 还是Youtube, 都可以说是某种个人发布平台, 只不过表现形式不同 &#8211; 文字, 图片, 视频等等. 可能最终他们会被当作一个很小的模块, 功能嵌入另外的产品中, 而不是彻底消失. 下面一段Yongfook介绍Sweetcron的视频, 值得一看:

 [1]: http://friendfeed.com/getfreeware "http://friendfeed.com/getfreeware"
 [2]: http://i.getfreeware.net/ "http://i.getfreeware.net/"
 [3]: http://code.google.com/p/sweetcron/wiki/Installation "http://code.google.com/p/sweetcron/wiki/Installation"
 [4]: http://www.your-site.com/ "http://www.your-site.com/"
 [5]: http://getfreeware.net/wp-content/uploads/2008/09/sweetcron-config.png
 [6]: http://getfreeware.net/wp-content/uploads/2008/09/sweetcron-database-config.png
 [7]: http://code.google.com/p/sweetcron/downloads/list "http://code.google.com/p/sweetcron/downloads/list"
 [8]: http://code.google.com/p/sweetcron/w/list "http://code.google.com/p/sweetcron/w/list"
 [9]: http://groups.google.com/group/sweetcron/topics "http://groups.google.com/group/sweetcron/topics"