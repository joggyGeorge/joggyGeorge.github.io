---
title: C#异步调用Process
date: 2021-08-01 18:30:00
tags: C#
---
最近pj要在后端C#里调用一个外部挂载的程序，为了防止阻塞前端，去查到了异步方法
[异步Console Program](https://haolaoshi.blog.csdn.net/article/details/84313108?utm_medium=distribute.pc_relevant_t0.none-task-blog-OPENSEARCH-1.control&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-OPENSEARCH-1.control)
[异步静默process应用](https://blog.csdn.net/wangzhichunnihao/article/details/111410953)
结果发现自己原来为了得到output，人为地WaitForExit，然而实际上我的gtkwave程序不需要output，所以直接把阻塞去掉应该就可以了。
***
后来发现还是有问题的：
把客户端和新开的gtkwave放在一个线程里会导致两者互相阻塞
对gtkwave的任何操作都有可能会被客户端的refresh cycle阻塞而不响应
所以去补了以下异步的知识
[异步全面解析](https://www.cnblogs.com/xiaoyaojian/p/4603238.html)
[自学汇总贴](https://my.oschina.net/u/2963604/blog/1818669)
用上面的方法重写了process.Start()，但是还是会碰到问题：gtkwave只响应一次，之后就不响应了，必须重新激活窗口才有新的反应。
***
最后问了学长，发现就是最简单的Start就完事了。。
因为新开了一个独立窗口不需要后端响应所以没有关系。。
