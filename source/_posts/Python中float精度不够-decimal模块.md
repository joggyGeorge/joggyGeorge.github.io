---
title: Python中float精度不够--decimal模块
date: 2021-08-05 20:20:54
tags: Python
---
如题，碰到这个问题后csdn了一下，贴几个过程。
[问题描述](https://blog.csdn.net/qq_39662044/article/details/76599167)
[模块中文说明](https://blog.csdn.net/weixin_37989267/article/details/79473706)
[英文文档](https://docs.python.org/3/library/decimal.html)
总之就是float进度太低，小数点后5位就不行了，但本身这个修改从数值上差距不大，但不能被看出来。
因此就用了decimal模块，支持整数和字符串输入，不支持浮点数输入，因为浮点数本来就不准了。