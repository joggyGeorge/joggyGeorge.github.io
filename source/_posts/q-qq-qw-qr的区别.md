---
title: 'q,qq,qw,qr的区别'
date: 2021-08-04 13:44:11
tags: Perl
---
<https://blog.csdn.net/sxlwzl/article/details/22740897>
q相当于单引号（quotation）
qq相当于双引号
qw可以用别的符号分隔元素（quotation word）
qw(a b c d) = ("a", "b", "c", "d")
qx代表创建正则表达式（quotation regex）
q xabcx 中x可以当作界限符（非空字符）
但qxabcx会被当做标识符