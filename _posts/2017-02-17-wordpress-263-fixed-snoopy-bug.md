---
layout: default
title: WordPress 2.6.3 修正了Snoopy库中的一个漏洞
published: true
author: gro
comments: true
date: 2008-10-26 09:10:38
tags:
    - unused link category
categories:
    - app
permalink: /2008/10/26/wordpress-263-fixed-snoopy-bug.html
---
WordPress官方发布了新版2.6.3, 在这个版本中修正了一个由Snoopy库带来的安全隐患. 尽管这个漏洞可能并太容易被利用, 但官方还是及时发布了更新文件.

在次下载WordPress 2.6.3 (英文版), 或者 WordPress 2.6.3 (中文版).

如果你现在使用的是2.6.2, 又不想下载安装整个软件包, 可以下载这两个文件, 分别覆盖对应的文件即可:

  * wp-includes/class-snoopy.php
  * wp-includes/version.php