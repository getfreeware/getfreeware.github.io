---
layout: default
title: 'WordPress插件推荐 #5'
published: true
author: gro
comments: true
date: 2008-06-23 11:06:14
tags:
    - unused link category
    - WordPress-插件
categories:
    - app
permalink: /2008/06/23/wordpress-plugins-5.html
---
对于访问量不大的blog, 似乎没有必要提及缓存的问题. 但是当你的blog越来越受欢迎, 访问量不断提高, 大量的用户请求就会造成对服务器的冲击. 如果你的某篇文章被Dugg, 并被&#8221;狂顶&#8221;至前几名和大量转载, 那这篇文章有可能会带来极高的访问量. 对于类似WordPress这样使用动态技术的blog平台, 频繁的网页请求意味着频繁的数据库操作, 这不仅造成了服务器资源的浪费, 也带来了潜在的危险. 这时你可以考虑启用缓存技术, 生成静态文件, 从而降低服务器的负担.

如果你使用WordPress, 那下面三个插件可以帮你实现缓存:

[WP-Cache 2.0][1]

WP-Cache 2.0是一个高效的缓存系统, 它可以极大提高网站的访问/响应速度. 它提供给访问者缓存的静态页面, 减少了重复操作数据库的过程, 从而大大节省了服务器资源, 加快了页面加载速度.

[WP Super Cache][2]

WP Super Cache 基于上面介绍的WP-Cache 2.0, 但是它还可以减少服务器解释动态脚本时所使用的资源. 对于普通的访问者, 它启用Super Cache, 对于登录或者发表过留言的访问者, 他调用WP-Cache 2.0的缓存.

Batcache

Batcache是刚发布不久的一个插件, 它与前两者缓存方式有所差别. 前两者对于共享主机的网站很有效, 但Batcache声称对类似企业内部多服务器环境同样适用. 比如它可以灵活的将2分钟内请求达到2次的页面缓存5分钟, 而这些时间, 频度是完全可以根据需要自行设置的(via [QOT][3]).

我使用了WP Super Cache, 按说明安装很顺利(dreamhost主机). 先入为主, 众家推荐, 以及安装简单是我选择它的原因. 至于效果还不很明显, 待日后在慢慢体验. 另外2个插件没有尝试, 所以也不敢写谁好谁坏. 上文很多地方凭理解, 没有查证, 也不知道是不是完全正确, 希望不要误人子弟.

WP Super Cache 0.6.4 的安装(dreamhost主机)

1. 上传插件至wp-content/plugins目录下

2. 后台激活插件

3. 到后台Settings-WP Super Cache菜单下启用插件(enable)

4. 然后再同一页面更新.htaccess文件即可

叙述的比较简单, 完整的安装说明请[移步到这里][4], 如果有任何问题,这里是[官方的FAQ][5].

 [1]: http://mnm.uib.es/gallir/wp-cache-2/
 [2]: http://wordpress.org/extend/plugins/wp-super-cache/download/
 [3]: http://www.quickonlinetips.com/archives/2008/06/batcache-wordpress-caching-plugin/
 [4]: http://wordpress.org/extend/plugins/wp-super-cache/installation/
 [5]: http://wordpress.org/extend/plugins/wp-super-cache/faq/