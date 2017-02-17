---
layout: default
title: 'Mozilla Weave – 在线服务与浏览器整合框架[Firefox扩展]'
published: true
author: gro
comments: true
date: 2008-07-02 10:07:08
tags: [ ]
categories:
    - app
permalink: /2008/07/02/mozilla-weave-firefox-extension.html
---
互联网技术的一种发展趋势是桌面应用与网络产品的融合, 其手段多是通过浏览器与各种网络服务的深度整合 &#8211; 这也可以解释为什么现在浏览器市场的争夺战如此激烈.

Mozilla Labs推出的产品Weave正对应了这种趋势, 简单说来, 它就是通过用户注册的单一帐号, 实现在多个终端(不同电脑的浏览器上)共享个人信息.

由于浏览历史, 书签, cookies等等信息都保存在网络服务器上, 所以, 不用担心由于单机硬件故障引起的数据丢失. 个人也可以无缝的在多台电脑上工作和处理个人事务. 而且, 通过共享信息, 例如书签, 还可以达到多人协同工作的目的.

举例说明, 我在公司浏览了某个网页, 回家想继续浏览却不记得网址. 我可以将网址写在纸上随身携带, 这样, 不管是在家, 或是在其他地方的电脑上, 我都可以输入网址浏览. 当然也可以使用社会化书签服务, 比如del.icio.us等等. 但是, 如果我的浏览记录(历史记录)保存在网络上, 我只要在浏览器中输入帐号, 就可以将公司的历史记录同步到家中的电脑, 岂不是更方便.

关于Weave的几个Use Case可以看这里 &#8211; [initial use cases][1].

在刚刚发布的0.2版中, Weave支持下列信息:

  * 书签
  * 历史记录
  * Cookies
  * 保存的秘密
  * 保存的表单数据
  * 标签(tabs)

完整的Release Note可以参考这里 &#8211; [Weave 0.2 Release Notes][2].

Weave作为Firefox的扩展发布, 使用前先要[下载安装][3]. 安装扩展后, 重启Firefox, 会弹出对话框, 根据提示点击下一步, 会出现如下界面:

[][4]

按左边的Get Started with Weave就会开始申请帐号. (在申请的过程中, 验证数字的图片始终不能显示, 所以我没能成功, 下面内容参考[Lifehacker][5]的相关文章.)

之后, 会提示要同步/备份的内容, 如下图:

[][6]

可以看到, 保存的密码和表单数据目前还是实验项目.

初次同步会比较慢, 耐心等候, 成功以后, 会出现成功提示:



在Firefox的状态栏上, Weave会增加一个图标, 它提供了登录, 退出, 立即同步等命令:



由于是实验性项目, 功能不一定完善, 所以我也不准备使用(况且, 安装出现问题), 关注一下就好, 毕竟是发展趋势.

 [1]: https://labs.mozilla.com/forum/index.php/topic,392.0.html "Weave initial use cases"
 [2]: http://wiki.mozilla.org/Labs/Weave/0.2/Release_Notes
 [3]: https://people.mozilla.com/~cbeard/weave/dist/latest-weave.xpi "mozilla weave download"
 [4]: http://getfreeware.net/wp-content/uploads/2008/07/weave-setup1.jpg
 [5]: http://lifehacker.com/397585/mozilla-weave-synchronizes-your-browsing-experience "Lifehacker"
 [6]: http://getfreeware.net/wp-content/uploads/2008/07/weave-setup2.jpg