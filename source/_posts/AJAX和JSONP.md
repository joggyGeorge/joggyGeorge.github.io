---
title: AJAX和JSONP
date: 2021-08-01 18:30:00
tags: JavaScript
---
AJAX: <https://www.liaoxuefeng.com/wiki/1022910821149312/1023022332902400#0>
JSONP: <https://www.cnblogs.com/dowinning/archive/2012/04/19/json-jsonp-jquery.html>

ajax是一种异步网络请求，用的是xmlhttprequest
jsonp用的是json脚本，功能相同

ajax的缺点是不能跨域传播，可以挂代理，但是html不限制远程调用js脚本，而js支持json，可以用json表示对象属性
综上，使用json作为传递数据的媒介可以用于异步网络请求

具体操作是将所需要的数据作为参数，外面包裹着本地已有的函数名，传回本地，也就是说外表是js脚本但实际上传递json对象数据
为了保证灵活性，我们可以将外部封装成可变参的方法，也就是说将所需的函数名提前传递给服务器，服务器根据传递的函数名做一次包裹
