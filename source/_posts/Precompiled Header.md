---
title: Precompiled Header
date: 2021-08-01 18:30:00
tags: C++
---
交叉编译Qt到arm核的时候碰见一个老熟人pch
专门为他查了一下：<https://blog.csdn.net/liubing8609/article/details/9064219>
原来pch在VeriSDK里也有，算是做一个工程时候的好习惯
所有容易重复编译的都提前编译放进去节约时间
