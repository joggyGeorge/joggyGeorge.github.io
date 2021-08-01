---
title: JSON
date: 2021-08-01 18:30:00
tags: JavaScript
---
补充一个json在线解析：
<https://www.json.cn/>

json作为一个方便网络端传输的文件格式，本身还是有很多名堂在里面的
这次是为了在C#中使用json，所以要先用Newtonsoft.Json库，然后查了一些资料，差不多知道个大概就先用上了
<https://www.cnblogs.com/mcgrady/archive/2013/06/08/3127781.html>
主要是原json格式文件的样子比较奇怪，是用JArray去存储键值对的，在我看来有点歪路子，调用格式的时候不能直接deserialize，所以遇到了一些麻烦

后来发现是对json的数据类型不熟悉
它有四种数据类型：
- JObject：最正常的对象
- JArray：数组类型，实际pj里用到的就是这个类型，我一直看错以为它是JObject
- JProperty：键值对，相当于Pair
- JValue：值类型，对照JProperty，相当于JProperty的一半

JOject取属性，就像对一个class取属性一样
JArray取子对象，就像对一个array取其中一项一样
JProperty应该用的是key\value

如果是比较特殊的json格式，就特殊对待
如果是一般的JObject格式，其实用Sererialize\Deserialize更方便，更傻瓜
