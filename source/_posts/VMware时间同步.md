---
title: VMWare时间同步
date: 2021-08-01 18:30:00
tags: VMWare
---
学校给了一个license过期的dc虚拟机，本来是不关机只挂起就能一直用了，结果突然license失效了
后来找到vmware关闭自动时间同步的帮助文档就好了
其实就是进入虚拟机的vmx配置文件，手动设置关闭自动时间同步，可能是vmware更新之后加了这个功能
<https://kb.vmware.com/s/article/1189?lang=zh_CN>
另外：如果关闭之后打不开虚拟机就把第一行tool_sync="0"去掉
***
后来其他人在FPGA课程上也碰到这个问题就重新写了一下解决办法贴出去了。现在补档一下：
fde过程中会用到dc，用的是license过期的虚拟机，本来复制解压出来不关机只挂起就能接着用
但现在有的vmware有自动同步时间功能
会自动同步时间，使license失效
办法是：
手动关闭功能
进入vmx配置文件，在最后加上
time.synchronize.continue = "0"
time.synchronize.restore = "0"
time.synchronize.resume.disk = "0"
time.synchronize.shrink = "0"
time.synchronize.tools.startup = "0"
time.synchronize.tools.enable = "0"
time.synchronize.resume.host = "0"
再打开虚拟机，如果依旧不行就重新解压虚拟机，重新改配置再打开
帮助文档：
<https://kb.vmware.com/s/article/1189?lang=zh_CN>
