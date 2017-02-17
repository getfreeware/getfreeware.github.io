---
layout: default
title: 去掉 Gmail 中的“on behalf of”
published: true
author: gro
comments: true
date: 2009-08-02 09:08:59
tags:
    - Google Mail
    - 电子邮件
    - 谷歌
categories:
    - app
permalink: /2009/08/02/remove-on-behalf-of-from-gmail.html
---
在 Gmail 中有这么一个功能，就是以其他邮件地址发送邮件（Settings – Accounts &#8211; send mail as）。也就是说，当你用 A@gmail.com 登陆后，可以以 B@gmail.com 或者 C@yourdomain.com 的身份发送邮件。我觉得这个功能很实用，如果你有好几个邮箱地址，它可以帮助你用一个邮箱管理其他邮箱。

但有个问题，你发送的邮件，在一些邮件系统中（比如 Outlook 和 Hotmail）会显示发送人为，A@gmail.com on behalf of B@gmail.com，或者是，A@gmail.com on behalf of C@yourdomain.com。很多用户都在 Google 的讨论组里抱怨，因为这样会暴露用户不想公开的邮件地址。

现在，Gmail 部分的解决了这个问题。如果用户使用的是自己的域名，并且服务商支持 POP 或者 IMAP，可以在 Settings – Accounts – send mail as – edit info 中选择使用自己的 SMTP 服务器。

 

当我们使用 Gamil 的服务器发送一封非 Gmail 地址的邮件时，Gmail 会根据发送协议要求，把 Gmail 的用户名加入到发送人字段中，这样可以防止邮件被划为垃圾邮件。现在，如果选择不使用 Gmail 服务器，那么邮件会直接交给用户指定的服务器，也就不会再出现 on behalf of 的字样了。

但是，如果以另外一个 Gmail 地址发送邮件，这个问题还是存在，希望 Gmail 团队能快点完善这个功能。