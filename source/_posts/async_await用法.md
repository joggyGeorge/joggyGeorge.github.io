---
title: async\await用法
date: 2021-08-01 18:30:00
tags: JavaScript
---
先贴网址
<https://segmentfault.com/a/1190000007535316>
写的蛮好的，前因后果都讲明白了
### 结论
在异步事件中，promise解决了回调陷阱，async\\await解决了promise的参数传递问题，长得也更像同步代码
### 细节
async函数返回promise对象，await对于任何函数都生效，一般函数会阻塞运行，但和async结合不会阻塞
promise在参数传递时，必须在then里使用箭头函数，而async\\await则是封装好的方法，外观上长得更像一般的【函数(变量)】的形式，不会碰到抽象的函数作为变量使用等问题。
可以说，promise开启了用对象解决异步非阻塞问题的先例，async封装了promise，并和await结合，使语法更加简化直观，是很好的拓展和优化。

当需要reject promise时，参见<http://www.ruanyifeng.com/blog/2015/05/async.html>
可以try...catch来捕获error
另外阮一峰日志看起来挺nb的，关注了

<https://www.cnblogs.com/zhaoshujie/p/11192036.html>
写的算是蛮好的了
主要是为了多线程任务
注意其中的限制是不能死锁，await返回TValue，await必须有返回值且是Task
但具体的应用还不是很清楚，只能走一步看一步了，毕竟要在js和C#间传输数据，报的错都很奇怪
