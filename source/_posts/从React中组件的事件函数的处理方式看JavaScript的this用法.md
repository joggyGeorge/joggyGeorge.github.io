---
title: 从React中组件的事件函数的处理方式看JavaScript的this用法
date: 2021-08-01 18:30:00
tags: React JavaScript
---
首先上JS的this用法总结：

- 在方法中，this 表示该方法所属的对象。
- 如果单独使用，this 表示全局对象。
- 在函数中，this 表示全局对象。
- 在函数中，在严格模式下，this 是未定义的(undefined)。
- 在事件中，this 表示接收事件的元素。
- 类似 call() 和 apply() 方法可以将 this 引用到任何对象。  

---

接着分别分析三种对React组件的事件函数的处理方式

1. bind
   ```javascript
   this.handleClick = this.handleClick.bind(this);
   ```
   这是最简单粗暴的，通过bind强行将这个函数绑定到this上（无条件）
2. 属性初始化器
   ```javascript
   handleClick = () => {
   console.log('this is:', this);
   }
   ```
   这是将这个方法作为一种属性传给了组件。也就是说，一个匿名函数变成了这个组件的属性handleClick
而属性的this永远是这个组件本身
3. render时使用匿名函数
这个方法比较复杂
首先看为什么不用匿名函数不行  
   ```javascript
   <button onClick={this.handleClick}>
   ```
   这里的this.handleClick作为一个函数传入了button的onClick事件中
如果点击了这个button，此时this不知道指向谁，现在全局对象中因此是window对象或者(严格模式)undefined
   ```javascript
   <button onClick={() => this.handleClick()}>
   ```
   
   这里传入的函数其实是一个匿名函数，在这个匿名函数中返回了this.handleClick()（也是一个函数）
因为是在事件中，所以this指向接受事件的元素button
而button不具有handleClick这个函数
因此向上寻找，找到了他的父组件Square，实际持有handleClick这一函数，所以能正确找到

从这段分析可以看出，当系统未找到函数、数据、方法时，
会向上寻找，不会向下寻找

但是管理多个子组件或者子组件之间通讯时，最好把数据放入父组件
因为数据传递可以向下穿透却不能向上穿透
也就是说，子组件不能随意修改父组件的数据
