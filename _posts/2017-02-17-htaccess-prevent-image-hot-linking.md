---
layout: default
title: 用.htaccess防止图片盗链(Prevent Image Hot Linking)
published: true
author: gro
comments: true
date: 2008-02-23 10:02:54
tags:
    - Linux
categories:
    - app
permalink: /2008/02/23/htaccess-prevent-image-hot-linking.html
---
 目前很多的虚拟主机都会支持.htaccess文件, 它最常见的用途是设置密码保护和自定义404页面. 实际上, 他可以做的不止这些.

.htaccess只是一个普通的文件, 用一个文本编辑器就可以打开, 编辑. 很多人习惯于Windows操作系统的用户认为这是一个没有文件名, 而扩展名为htaccess的文件, 实际上他是一个没有扩展名的文件(文件名是.htaccess, 类Unix系统有别于Windows的地方). 以&#8217;.&#8217;开头的文件, 在类Unix系统中通常是隐藏的, 所以在你的虚拟主机上你想看到他的话仅用ls是不行的, 一定要加-a这个参数.

图片盗链就是说, 其他网站(网站A)引用/链接存储在你的虚拟主机空间里的图片, 这样一来, 网站A就不用费力上传图片到他自己的空间, 又节省了他自己的带宽. 因为每次浏览者看到的图片, 都链接自你的空间. 如果引用数量巨大, 必然造成自己的资源浪费和虚拟主机空间效率下降.

用.htaccess文件, 可以防止其他网站盗用你的图片, 语法大致如下:

> RewriteEngine on
RewriteCond %{HTTP_REFERER} !^http://yourdomain.com.*$ [NC]
RewriteCond %{HTTP_REFERER} !^http://www.yourdomain.com.*$ [NC]
RewriteRule .*.(gif|jpg|jpeg|bmp)$ http://www.yourdomain.com/stophotlinking.html [R,NC]

第二,三行yourdomain要换成你的域名, 第四行的gif|jpg|jpeg|bmp是保护的图片类型(扩展名),常见的还有png格式, 根据个人喜好也可以加上. 之后的网址是转向网址, 就是说如果其他人盗用了你的链接, 那个引用的页面就会自动跳转到你指定的页面. 但是我尝试过以后发现, 并不能转到网址. 实际上你可以把那个网址换成一个图片的链接, 比如, 为什么是xjpg呢, 其实就是jpg的图片, 因为你已经阻止了其他人引用你的jpg文件, 所以将文件扩展名改为xjpg, 其他的网址才能显示出来.

当然还有简单的做法, 看看这个网站: Htaccess Disable Hotlinking Code Generator. 它可以帮助你在线生成防止盗链的.htaccess文件内容, 你要做的就是填写一些相关信息.

****check if your images can be hotlinked**** &#8211; 输入一个来自你的网站的图片链接, 即可检查别人是否可以盗链你的图片

****urls to allow to hotlink**** &#8211; 允许链接图片的网址, 当然是你自己的网站网址, 或者你拥有其他网站, 把它们也写上

****or &#8211; image to replace with (if desired)**** &#8211; 替代图片, 别人盗链的时候会显示这个图片(上面提到的xjpg文件)

****files to block**** &#8211; 你想保护的文件类型, 默认的是gif jpg jpeg bmp, 一般还有png格式.

填好了这些, 点generate就会生成.htaccess文件的内容了:)

如果你想了解关于.htaccess更详细的信息, 可以浏览下面的相关链接.

相关链接:

.htaccess使用指南 &#8211; [http://hellobmw.com/archives/using-htaccess.html][1]

.htaccessEditor &#8211; [http://www.htaccesseditor.com/sc.shtml][2]

Htaccess Disable Hotlinking Code Generator &#8211; [http://www.htmlbasix.com/disablehotlinking.shtml][3]

Dreamhost Wiki &#8211; [http://wiki.dreamhost.com/KB\_/\_Unix\_/\_.htaccess_files][4]

 [1]: http://hellobmw.com/archives/using-htaccess.html "http://hellobmw.com/archives/using-htaccess.html"
 [2]: http://www.htaccesseditor.com/sc.shtml "http://www.htaccesseditor.com/sc.shtml"
 [3]: http://www.htmlbasix.com/disablehotlinking.shtml "http://www.htmlbasix.com/disablehotlinking.shtml"
 [4]: http://wiki.dreamhost.com/KB_/_Unix_/_.htaccess_files "http://wiki.dreamhost.com/KB_/_Unix_/_.htaccess_files"