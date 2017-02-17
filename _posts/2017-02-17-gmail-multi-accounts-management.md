---
layout: default
title: '[Gmail]多账户管理技巧 – Gmail高级搜索,过滤器及其他'
published: true
author: gro
comments: true
date: 2008-06-08 01:06:54
tags:
    - Google
    - Webware
    - 谷歌
categories:
    - app
permalink: /2008/06/08/gmail-multi-accounts-management.html
---
这篇文章主要讲如何用一个Gmail帐号管理其他若干个Gmail帐号, 其中主要涉及到Gmail的高级搜索操作符(Advanced search operators)和过滤器(Filter)的设置. 如果你对此没有任何兴趣, 就不必再费时间往下看了^^.

其实不知道写这样一篇文章有没有必要.

> 第一, 不确定是不是有人像我一样用多个Gmail邮箱处理日常事务, 对公对私, 网站管理等等, 我都申请了不同的帐号. 这算是一个经验共享, 也算是一个个人总结, 因为一直以来都在&#8221;摸索中前进&#8221;.
> 
> 第二, 即使有多个Gmail的帐号, 可能很多人也懒得折腾, 只是每次都登录不同的帐号去收发邮件 &#8211; 其实不必, 完全可以在一个帐号中管理.
> 
> 第三, Gmail支持POP3, 现在更支持IMAP, 所以如果你习惯用邮件客户端的话 &#8211; 比如Outlook, Thunderbird之类, 也可以, 但web方式的好处显而易见, 不需要浪费本机的空间, 不需要在多台主机上重复设置. 并且IMAP已经解决了POP3的一些弊端, 比如它的时时连接性, 双向同步等优点, 客服了POP3丢消息, 重复下载的不足. 本文不讨论IMAP和POP3的使用, 上面某些词汇也没有经过查证, 可能有些不准确, 希望指正.
> 
> 第四, 就是所谓的管理技巧, 可能言过其实, 但我想不到更合适的词语. 文章里不足和不准确的地方希望能得到纠正, 不罗嗦, 开始了.

假设我有如下Gmail邮箱: manager@gmail.com, job@gmail.com, friends@gmail.com. job用来找工作用, friends用来和密友联系, manager来管理这两者.

> 1. 设置以job和friends的身份发送邮件. 这个不难, 登录manager, 在Settings-Accounts中有一项Send mail as的设置, 允许你以其他邮件地址发送邮件(不限于Gmail). 点击Add another email address, 在弹出对话框中, 输入job所对应的邮件地址, 点下一步, 点发送验证. 然后进入job的邮箱, 在收到的确认信中点确认链接确认. 这时回到manager邮箱, 在撰写邮件的时候, from一栏就会多出一个选项, job. friends邮箱也如法炮制. 现在你就可以在manager帐号中以job或者friends的身份发邮件了.
> 
> 
> 
> 2. 在manger的邮箱中接收其他邮箱的信件. 最简单的做法是在job帐号中启用Forwarding(转发) &#8211; Settings->Forwarding and POP/IMAP, 将邮件转发到manager的邮件地址, 但这样有一个弊病, 就是被Gmail归为spam的垃圾邮件不会转发, 但问题是有时候Gmail会错误的把正常邮件标记为spam. 所以我们可以创建过滤器来转发所有的邮件(包括spam). 如果你开启了刚刚说的Forwarding, 把它禁用. 然后进入settings-filters- create a new filter, 在Has the words一项加入: in:inbox OR in:spam. 点击下一步(弹出对话框点确定), 然后选Forward it to, 并加入manager的邮件地址, 保存即可. 这样, 所有到达inbox和spam标签下的邮件都会被转发给manager了. 你还可以根据需要勾选skip the inbox, mark as read等等.
> 
> 
> 
> 3. 在manager帐号中创建过滤器和标签分类. 这一步不必须, 因为完成前2步你已经可以在manager帐户中正常收发job和friends的邮件. 但我不喜欢他们都一股脑混进inbox, 所以我创建了两个过滤器, 在过滤器has the words一项中加入: to:job@gmail.com OR cc: job@gmail.com, 并在下一步中选择skip the inbox, apply the label. 意思是, 如果邮件的收件人是job, 或者转发给job的邮件, 都不进入inbox, 而是应用一个我预先定义好的标签, 比如job. 对发送给friends的信件, 也创建一个类似的过滤器即可.

总结, manager只是为了说明方便, 实际上, 用job就可以管理friends帐户和其他帐户, 没有必要单独设立manager. 上文涉及到的in, to, cc等为Advanced search operators, 除了在过滤器中使用, 也可以在邮件搜索时使用. 更全面的操作符请看这里: Using advanced search.

问题:

如果用密件抄送一封邮件给job(bcc to job), 那在manager中, 它会出现在inbox中, 因为Gmail不支持bcc搜索.

由于时间有限, 写的很乱很罗嗦, 肯定也有错误不足, 望指正, 见谅.