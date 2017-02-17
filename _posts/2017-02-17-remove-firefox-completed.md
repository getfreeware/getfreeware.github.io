---
layout: default
title: 如何彻底删除firefox
published: true
author: gro
comments: true
date: 2008-03-10 05:03:30
tags:
    - Firefox
categories:
    - app
permalink: /2008/03/10/remove-firefox-completed.html
---
从控制面板中卸载firefox之后, 原来保存的书签, 下载的插件等信息并不会删除. 如果想彻底从系统中清除这些信息, 或者想重新安装一个&#8221;干净&#8221;的新版firefox怎么办呢?

如果想彻底的卸载firefox请参考以下步骤:

1. 退出正在运行的firefox, 并从添加删除程序中卸载firefox;

2. 删除firefox的安装文件夹, 默认在&#8221;C:Program filesMozilla Firefox";

3. 删除下列隐藏文件(夹):



  * **Windows 2000/XP**: C:Documents and SettingsLocal SettingsApplication DataMozillaFirefox
  * **Windows Vista**: C:UsersAppDataLocalMozillaFirefox
  * **Windows Vista**: The C:UsersAppDataLocalVirtualStoreProgram FilesMozilla Firefox
  * **Windows XP/Vista**: C:WINDOWSPrefetchFIREFOX* (**所有以FIREFOX开头的文件**)
  * 如果按住了Quality Feedback Agent, 打开%APPDATA%TalkbackMozillaOrg 文件夹(可以在开始-运行中打开)并删除所有类似于&#8221;Firefox&#8221; 的文件夹, 比如, &#8220;Firefox10&#8221; &#8220;Firefox15&#8243; 和&#8221;Firefox2&#8221;.

另外还有一些注册表项, 需要用修改注册表工具进行修改, 不建议操作.

4. 删除firefox的用户资料数据(包括bookmarks, passwords, cookies, preference settings and added extensions等信息), 打开下面的文件夹, 并删除其中的firefox文件夹即可:

  * Windows 95, 98, and ME: C:WindowsApplication DataMozilla 或者 C:WindowsProfilesApplication DataMozilla
  * Windows 2000 and XP: C:Documents and SettingsApplication DataMozilla
  * Windows Vista: C:UsersAppDataRoamingMozilla

从Firefox 3.0版开始, 卸载Firefox的时候可以选择&#8221;删除个人数据和个性化信息&#8221;, 这样就不必做上述繁琐的操作了.

参考资料:
  
Uninstalling Firefox &#8211; [http://kb.mozillazine.org/Uninstalling_Firefox][1]
  
Finding the profile folder &#8211; [http://kb.mozillazine.org/Profile\_folder\_-\_Firefox#Finding\_the\_profile\_folder][2]

 [1]: http://kb.mozillazine.org/Uninstalling_Firefox "http://kb.mozillazine.org/Uninstalling_Firefox"
 [2]: http://kb.mozillazine.org/Profile_folder_-_Firefox#Finding_the_profile_folder "http://kb.mozillazine.org/Profile_folder_-_Firefox#Finding_the_profile_folder"