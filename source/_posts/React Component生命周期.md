---
title: React Component生命周期
date: 2021-08-01 18:30:00
tags: React
---
[![WzdsO0.jpg](https://z3.ax1x.com/2021/08/01/WzdsO0.jpg)](https://imgtu.com/i/WzdsO0)

componentWillMount和componentDidMount是最基本的
必须保证render是纯净只渲染组件的
componentWillReceiveProps可以安全获取前后两个state的props
shouldComponentUpdate其实是一个判断句，true继续update，false返回self-loop
