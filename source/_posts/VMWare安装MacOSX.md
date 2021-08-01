---
title: VMWare安装MacOSX
date: 2021-08-01 18:30:00
tags: VMWare
---
因为毕设要测试macos平台的可行性，所以想用虚拟机装一个macos，结果碰到好多不兼容的问题，果然苹果内生系统是恶心呀
附教程链接：
[OSX10.11](https://blog.csdn.net/viafcccy/article/details/83053970)
[百度经验](https://jingyan.baidu.com/article/363872ec206a356e4ba16f30.html)
但是笔记本装不上，后来发现CPU必须是Intel才行，而我的MagicBook是锐龙版的，那没事了，换台式机
结果台式机也装不上，查到是VMWare和OS系统不匹配，VMWare Workstation 15必须装新的OSX 10.15 Catalina才行
[VMWare与OSX不匹配](https://blog.csdn.net/MicePro/article/details/104526639/)
而且原帖贴的下载链接也失效了，那只好自己再找找了
后来又碰到好多问题，果然黑苹果很麻烦啊。。
***
自己找了一个10.15的dmg，然后用dmg2iso转格式，结果蓝屏了还是不能用，只能老老实实找了个10.14的iso
装到一半说副本损坏，结果苹果坏得很，其实只是同步网络发现时间戳不对检测到黑苹果了，要把网络关了，手动改时间
[改时间](https://zhuanlan.zhihu.com/p/91707695)
现在还在装...
***
总算装好了，几个小设置都要试一下。beamoff设为登陆项关闭一些设置可以提速
最后把安装包和虚拟机都打包备份一下
***
找到一个可以在AMD上装mac的教程，现在还没时间看，贴出来
[Mac on AMD](https://blog.csdn.net/xiaocheng0404/article/details/106963575/?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-1&spm=1001.2101.3001.4242)
