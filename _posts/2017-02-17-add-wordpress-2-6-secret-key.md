---
layout: default
title: 如何为WordPress2.6添加secret key
published: true
author: gro
comments: true
date: 2008-07-27 05:07:50
tags:
    - unused link category
categories:
    - app
permalink: /2008/07/27/add-wordpress-2-6-secret-key.html
---
在WordPress2.6版中, 引入了3个secret key以加强WP的安全性能. 要设置这些key并不麻烦, 如下操作即可:

1. 首先, 打开wp-config.php.找到下面三行:

> define(&#8216;AUTH_KEY&#8217;, &#8216;put your unique phrase here&#8217;); // Change this to a unique phrase.   
> define(&#8216;SECURE\_AUTH\_KEY&#8217;, &#8216;put your unique phrase here&#8217;); // Change this to a unique phrase.   
> define(&#8216;LOGGED\_IN\_KEY&#8217;, &#8216;put your unique phrase here&#8217;); // Change this to a unique phrase.

这就是需要做修改的地方.

2. 然后打开这个网址: [http://api.wordpress.org/secret-key/1.1/][1]. 这个网址会产生随机的key, 长度都是60+的.

3. 接下来, 只要用这些生成的代码替换config文件中相应的部分就行了.

你不需要记住这些随机产生的key. 如果你的cookie被拦截, 这些繁琐的文字可以有效的防止他人复制你的cookie. 2.6版中还新添加了对SSL连接的支持.

如果你用的是WordPress2.5版, 那config文件中只需要设置一个secret key:

> define(&#8216;SECRET_KEY&#8217;, &#8216;put your unique phrase here&#8217;); // Change this to a unique phrase.

官方也提供了一个generator, 网址在这里: [http://api.wordpress.org/secret-key/1.0/][2]

我建议使用WP的朋友添加secret key以提高WordPress的安全性. 关于config文件的详尽说明以及secret key的重要性, 请参考官方文档: [Editing wp-config.php][3].


  Technorati Tags: WordPress,secret key


 [1]: http://api.wordpress.org/secret-key/1.1/ "WordPress 2.6 secret keys generator"
 [2]: http://api.wordpress.org/secret-key/1.0/ "WordPress 2.5 secret key generator"
 [3]: http://codex.wordpress.org/Editing_wp-config.php "WordPress - Editing wp-config.php"