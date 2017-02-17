---
layout: default
title: '利用.htaccess实现Feed跳转的具体方法[WordPress]'
published: true
author: gro
comments: true
date: 2008-11-14 11:11:44
tags:
    - htaccess
categories:
    - app
permalink: /2008/11/14/htaccess-feed-redirect-wordpress.html
---
 今天看到Shawn’s Blog一篇文章抱怨Feedsky的服务, 并且介绍了Feed跳转的方法. 我也一直在用.htaccess文件控制Feed的指向, 在这里共享一下具体的实现方法, 并顺便总结一些和Feed相关的知识, 分成下面几个方面:&#160; 

  1. 关于WordPress的feed输出格式 
  2. 关于.htaccess文件和URL重写 
  3. 关于Feed托管(烧录)服务 
  4. 利用.htaccess实现Feed无缝切换 

国内很多blogger喜欢用子域名来绑定Feed, 大多类似这样的格式: http://feed.getfreeware.net. 我不知道具体从什么时候开始(也许是Feedsky提供子域名绑定服务以后), 这种形式的feed输出开始流行起来, 我访问过得国内blog站点, 十有八九都会提供并推荐给读者用这种地址订阅RSS输出.

但是我更倾向于使用WordPress原始的Feed形态, 一来, 增加并修改子域名的A记录, CNAME记录比较麻烦(可能是曾经操作失误留下的阴影), 二来, 我在猜想, 使用网站的一级域名为基础发布Feed, 会不会对PR值有所贡献.(而且在Google Webmaster Tools里面可以被自动侦测到).



完成同一件事情, 有很多种方法, 对于使用者来说, 自己熟悉, 容易实现, 并利于以后维护的方法是首选. 选择用.htaccess文件控制Feed, 我要做的只是在根目录下修改这个文件, 一旦发生错误, 我只要还原成备份的文件就可以了. 而且我不需要等域名生效的时间, 可以立马观察结果.

**1. 关于WordPress的feed输出格式**

我们最好先了解一下WordPress会输出什么样的Feed格式, 这样在写RewriteRule的时候会更清楚明白, 更灵活.

对于多数模板, 都会使用bloginfo(&#8216;rss2_url&#8217;)这个tag来获取Feed地址. 如果是新安装的WordPress, 输出格式是这样的: http://example.com/?feed=rss2, 这里要注意的是, 参数指定了输出rss2.0格式的feed, 有些人喜欢用atom的,那么输出的地址格式是这样的: http://example.com/?feed=atom.

当然, 多数人会启用permalink, 也就是固定链接, 自定义链接格式, 随便怎么称呼吧. 当你选择了一种固定链接以后, **bloginfo(&#8216;rss2_url&#8217;)**输出结果会变为: 

  * http://example.com/feed, 或者是, 
  * http://example.com/feed/ 

如果你选择的固定链接格式没有以”/”结尾, 比如本站使用像这样[http://getfreeware.net/archives/617.html][1]格式, 会输出上述第一种不以”/”结尾的Feed格式. 反之, 固定链接如果以”/”结尾, 那么Feed的地址也相应的会输出以”/”结尾. 有些阅读器把两个地址分别对待，比如Google Reader；而有些阅读器会将后者自动改为前者，比如鲜果。

好了, 大体上知道这些够用了, WordPress官方文档有相关的资料: [http://codex.wordpress.org/WordPress_Feeds][2], 但实际上它没写清楚什么时候输出的Feed会以”/”结束, 所以这一点当初让我困惑了好久…

&#160;

**2. 关于.htaccess文件和URL重写（mod_rewrite）**

在Apache服务器中，.htaccess文件(或者"分布式配置文件")提供了针对每个目录改变配置的方法，即在一个特定的目录中放置一个包含指令的文件，其中的指令作用于此目录及其所有子目录。（查看Apache2.2版.htaccess文件说明）

Apache的mod\_rewrite是提供了强大URL操作的杀手级的模块，可以实现几乎所有你梦想的URL操作类型，其代价是你必须接受其复杂性，因为mod\_rewrite的主要障碍就是初学者不容易理解和运用，即使是Apache专家有时也会发掘出mod_rewrite的新用途。（查看Apache2.2版URL重写指南）

我们需要将mod_rewrite模块提供的一些指令加到网站根目录下的.htaccess文件中， 使得用户访问网站的时候，指令生效并做出相应的处理。

3. 关于Feed托管(烧录)服务

很多blogger都会使用诸如Feedburner或者Feedsky的托管服务。

使用托管的优点是减轻自己服务器的负担，可以获得一些免费增值服务，比如数据统计等，还有就是可以通过托管服务赚钱。

但是缺点也很明显，Feed托管以后，要使用托管商的网址，国外的托管商在国内访问受限制，而国内托管商服务不稳定，没有公信力。

那么两全其美的方法就是，仍然使用自己的域名输出Feed，但在“背地里”将Feed转向自己烧录的地址。这样就可以在不影响订阅用户的前提下，自由的切换Feed转向。下面的内容就是具体的实现方法。

4. 利用.htaccess实现Feed无缝切换

我的.htaccess文件是这样写的：

> &#160;
> 
>   1.  
>   2. RewriteEngine On 
>   3. RewriteBase / 
>   4. RewriteCond %{QUERY_STRING} ^feed=(rss|rss2|rdf|atom|feed)$ [NC,OR] 
>   5. RewriteCond %{REQUEST_URI} ^/(feed|wp-atom|wp-feed|wp-rss|wp-rdf)(.*)$ [NC] 
>   6. RewriteCond %{HTTP\_USER\_AGENT} !^.*(Gecko|MSIE|Opera|FeedBurner|FeedValidator|Feedsky|xianguo-rssbot) [NC] 
>   7. RewriteRule (.*) http://feedproxy.google.com/getfreeware? [L,R=307] 
>   8. RewriteCond %{REQUEST_FILENAME} !-f 
>   9. RewriteCond %{REQUEST_FILENAME} !-d 
>  10. . RewriteRule . /index.php [L] 
>  11. .  

如果你懒得花时间了解这些指令，可以直接将其复制到服务器的.htaccess文件中，**记得把其中的蓝色地址换成你自己的烧录地址**。

简单说明一下：

第4行，匹配形如http://example.com/?feed=rss2的请求；

第5行，可以匹配形如http://example.com/feed或者是http://example.com/feed/ 的请求；

第6行，排除烧录服务的Feed抓取（避免陷入无限循环），并**排除用户通过浏览器的直接请求**，比如，用户直接在浏览器输入http://example.com/feed/，不会发生跳转；

第7行，将符合条件的请求进行307重定向到我的Feed地址；

第8-10行，是启用固定链接后WordPress自动加入的。

这样一来，只要改变第7行的烧录地址（蓝色部分），就可以实现在Feedburner和Feedsky间的无缝切换。而且，当用户直接在浏览器中原始输出的地址，也不会暴露跳转地址，但用户使用阅读器订阅的时候，看到的则是跳转后的Feed。

我写的还不是很严谨，对于一些细节没有仔细处理（比如第6行会排除掉某些不太规范的阅读器），但是目前基本符合我的需要，也应该符合大多数blogger的需要，花了整整2个晚上构思和完成这篇文章，希望能对自己建站的朋友有用:)

 [1]: http://getfreeware.net/archives/617.html "http://getfreeware.net/archives/617.html"
 [2]: http://codex.wordpress.org/WordPress_Feeds "http://codex.wordpress.org/WordPress_Feeds"