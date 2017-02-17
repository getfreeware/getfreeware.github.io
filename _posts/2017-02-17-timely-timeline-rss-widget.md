---
layout: default
title: '贴历 – 时间轴RSS订阅小工具[Widget]'
published: true
author: gro
comments: true
date: 2008-11-11 11:11:36
tags:
    - timely
    - Widget
    - 贴历
categories:
    - app
permalink: /2008/11/11/timely-timeline-rss-widget.html
---
[][1]贴历(Timely)是一个基于时间轴的RSS订阅工具.

用户可以自己添加喜欢的RSS源(也就是常说的feed), 这些RSS输出会按照时间顺序显示出来. 比如添加了免费软件资讯站的feed, 本站发表文章时, 贴历就会在文章发表所对应的时间点上增加一个标记, 显示这一时刻发表的文章, 看左图更形象(看不清就猛击图片一次, 用鼠标左键).

右上方的桔红色圆点就是发表文章的标记, 那是本站先前发表的IETester 0.2.3 下载一文. 上部显示日期, 右侧竖排显示了24个小时, 可以确定发表文章的大概时间. Widget下部是一些控制按钮, 可以控制时间轴的走向, 也就是显示前几天, 后几天的情况等等.



**设置方法**&#160;

  * 使用这个小工具很方便, 首先到Timely网站注册: [http://timely.hiiir.com/][2], 然后查收邮件**确认信**进行确认; 
  * 之后登陆系统(如果你点击确认信中的验证链接, 现在应该已经登陆进系统了, 可以忽略这一步), 找到**建立新贴历**的链接: [http://timely.hiiir.com/Poster/new][3] 
  * 这时看到的是贴历的管理/添加界面, 如下图(记得猛击图片一次, 用鼠标左键), 首先**设置贴历的名称, 编码, 说明等:   
    [][4]** 
  * 好了之后点下一步, **添加RSS源**, 比如我添加了本站的feed地址: , 标题设置为getfreeware, 选择RSS图标其实是选择不同颜色, 根据个人喜好设置吧, 好了之后点**新增一组RSS**按钮; 
  * 进入下一步, 是**选择Widget的外观**, 依个人喜好选择即可; 
  * 点下一步**预览**并**取得可以嵌入blog的代码**; 
  * 最后, 把取得的代码粘贴到自己blog的模板中, 即可显示出来, 实例看本站左侧下方即可; 

试用后觉得这个小工具还挺有意思, 除了免费使用之外, 贴历还是一个广告平台, 可以利用这个工具赚钱. 虽然不知道是不是有门槛限制, 也不知道收益如何, 但是通过widget进行营销确实是不错的想法.

不足之处是, 新用户只能在一个贴历中增加最多3个RSS源(我添加了自己的, 老所的和lifehacker的作为实验, 哈哈), 而且新用户只能添加一个贴历, 想增加更多的贴历, 需要使用礼物金购买.

另外一个很不方便的地方是, 如果我在贴历中修改了RSS设置(比如增加新的RSS), 最后生成的代码会变化(传递给js脚本的一个参数Time值). 比如我第一次只增加了一个feed, 生成了一段代码. 之后编辑这个贴历, 又增加了两个feed, 再生成的代码中的Time值就会更新. 我本以为必须要在模板中使用第二次生成的代码才能生效, 但后来发现使用旧代码也会显示3个feed的信息. 那这个参数是做什么用的, 很迷惑人啊…:S

贴历(Timely) [via 分享网络2.0]

 [1]: http://getfreeware.net/wp-content/uploads/2008/11/timely-0.png
 [2]: http://timely.hiiir.com/ "http://timely.hiiir.com/"
 [3]: http://timely.hiiir.com/Poster/new "http://timely.hiiir.com/Poster/new"
 [4]: http://getfreeware.net/wp-content/uploads/2008/11/timely-1.png