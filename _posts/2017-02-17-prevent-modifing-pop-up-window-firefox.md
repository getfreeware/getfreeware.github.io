---
layout: default
title: 防止网站修改Firefox弹出窗口
published: true
author: gro
comments: true
date: 2008-02-26 11:02:39
tags:
    - Firefox
categories:
    - app
permalink: /2008/02/26/prevent-modifing-pop-up-window-firefox.html
---
有些网站的会修改弹出窗口的外观, 比如隐藏地址栏,工具栏,有时你甚至不能调整弹出窗口的大小.[][1]
  
在Firefox中, 你可以对此作出相应的设置来控制弹出窗口的状态. 打开about:config页, 在过滤栏(Filter)中输入dom.disable\_window\_open_feature, 出现的条目及意义如下:



close: 是否防止关闭按钮被禁用.
  
directories: 是否防止收藏栏被禁用.
  
location: 是否防止地址栏被禁用.
  
menubar: 是否防止菜单被禁用.
  
minimizable: 是否防止最小化功能被禁用.
  
personalbar: 是否防止自定义的工具栏被禁用(?).
  
resizable: 是否防止调整窗口大小功能被禁用.
  
scrollbars: 是否防止滚动条被禁用.
  
status: 是否防止状态栏被禁用.
  
titlebar: 是否防止标题栏被禁用.
  
toolbar: 是否防止导航栏被禁用.

来自: [http://kb.mozillazine.org/Prevent\_websites\_from\_disabling\_new\_window\_features][2]


  Technorati Tags: firefox,about:config,popup window


 [1]: http://getfreeware.net/wp-content/uploads/2008/02/firefox-dom.jpg
 [2]: http://kb.mozillazine.org/Prevent_websites_from_disabling_new_window_features