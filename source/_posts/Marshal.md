---
title: Marshal
date: 2021-08-01 18:30:00
tags: C#
---
MarshalAs是提供向非托管代码封送数据时的规则。比如String或StringBuilder型，传递给非托管代码的时候可能是LPStr LPWStr BStr等等。你通过MarshalAs特性告诉.NET应该封送成什么类型。
Marshal就是把一个结构（类）序列化成一段内存，然后送到另一个进程（.net中Application domain)中供另一个进程中的函数使用。
比如你的一个结构struct{
Pen pen;
}s; s是一个指向已有的Pen对象的引用，当你把s传给本进程中的一个函数f时,f可以很容易地找到pen的实际对象，但如果你把s传到另外一个进程时，甚至是另外一台机器上的进程时，这个进程就没办法找到pen的实际内容。Marshal技术则可以把pen对象中的所有实际内容按规则放到一个缓冲中，（所有的引用或指针都要转换成实际对象）然后把缓冲中的内容送到另一个进程，函数调用完成再用同样方式把结果返回来。
在RPC,Interop,COM中Marshal应用很多。
