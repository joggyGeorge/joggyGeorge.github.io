---
title: event.target.value
date: 2021-08-01 18:30:00
tags: JavaScript
---
给出两个例子
1. 
```html
<select id="test1" />
```
```javascript
document.getElementById("test1").onchange = (event) =>
    console.log(event.target.value);
````
2. 
```html
<select id="test2" onchange=handleSelect(this) />
```
```javascript
let handleSelect = (event) =>
    console.log(event.value);
```

为什么一个是event.target.value一个是event.value呢？
因为实际上可以将event换成this
例1的this是onchange事件，所以可以有target
例2的this是select组件，所以它没有target而直接具有value属性
