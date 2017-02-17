---
layout: default
title: 关闭WordPress2.6的自动保存和文章版本控制功能
published: true
author: gro
comments: true
date: 2008-08-17 05:08:55
tags:
    - unused link category
categories:
    - app
permalink: /2008/08/17/disable-wordpress-revision-control.html
---
现在讨论这个似乎已经很火星了, 但是我刚刚升级到2.6, 所以还是记录一下吧.

**自动保存不是2.6的新功能, 如果想禁用有如下方法:**

第一, 使用WLW或者其他工具写文章, 这样就避免了自动保存. 这是最为推荐的一种办法, 不用加插件, 不用改代码, 而且WLW很好用.

第二, 如果喜欢在浏览器中写文章, 又想禁用自动保存功能, 那我推荐使用插件 &#8211; [disable-autosave][1].

第三, 直接修改WP核心文件. 不推荐这种方法, 为什么呢? 首先是, 以后每次升级WordPress都要手动修改一次, 很麻烦. 其次, 从使用者的角度来说, 我们尽可能少修改核心文件是上策. 如果你喜欢捣鼓, 可以参考这篇文章中的办法来修改 &#8211; [如何管理WP自动保存功能][2].

**再来说说如何禁用文章版本控制, 也就是Post Revision的功能:**

第一, 推荐使用插件 &#8211; [disable-revisions][3]. 推荐插件的原因基本同上.

第二, 修改wp-config.php文件. 在其中添加: 

define(&#8216;WP\_POST\_REVISIONS&#8217;, false);

在官网上有一篇关于[Revision Management][4]的文章, 写的不是很清楚, 但可以参考一下. 上面的两个插件来自同一个作者, 他还制作了一个插件, 同时禁用自动保存和文章版本控制功能, [原文在这里][5].

鲜果认领, 读者请忽略:

BANG72A3DBCA6149D0A7E17A54D3XIANGUO

 [1]: http://exper.3drecursions.com/wp/disable-autosave.zip "disable-autosave wodpress plugin"
 [2]: http://www.thinkagain.cn/archives/973.html "如何管理WP自动保存功能"
 [3]: http://exper.3drecursions.com/wp/disable-revisions.zip "disable-revisions wordpress plugin"
 [4]: http://codex.wordpress.org/Revision_Management "Revision Management"
 [5]: http://exper.3drecursions.com/2008/07/25/disable-revisions-and-autosave-plugin/ "disable-revisions-and-autosave wordpress plugin"