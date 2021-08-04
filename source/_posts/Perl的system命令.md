---
title: Perl的system命令
date: 2021-08-04 15:01:00
tags: Perl
---
<https://cn.perlmaven.com/running-external-programs-from-perl>
system可以直接运行字符串，也可以运行字符串数组，将参数一个一个弹进去。
直接运行字符串可以由shell扩展通配符，数组参数不行。
但直接运行字符串有攻击风险，数组进入则可以规避。