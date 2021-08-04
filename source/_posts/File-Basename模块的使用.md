---
title: 'File::Basename模块的使用'
date: 2021-08-04 12:54:27
tags: Perl
---
<https://www.cnblogs.com/ec04/archive/2012/11/21/2780146.html>
一共三个函数，fileparse, basename, dirname。
对于一个完整路径文件:'C:\User\Desktop\test.pl'
有basename, dirname, suffix
basename = test
dirname = C:\User\Desktop\
suffix = .pl

fileparse返回这三个属性，basename和dirname只返回对应的一个属性。

这个模块应该是对路径根据分隔符进行split，最后一个去除suffix就是basename，剩下的是dirname
所以是有特殊情况的，如果输入的是个文件夹，basename就是最后一个。