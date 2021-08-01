---
title: IPCRenderer\IPCMain
date: 2021-08-01 18:30:00
tags: Electron
---
IPCRenderer和IPCMain联合应用，功能是在主进程和其他渲染进程之间传递事件
[IPCRenderer](https://www.electronjs.org/docs/api/ipc-renderer)
[IPCMain](https://www.electronjs.org/docs/api/ipc-main)

主要有两个参数，channel和listener:
- channel是自定义字符串，只是起个名字
- listener是回调函数，一旦被call了会发生什么

主进程在这里主要指事件和行为
渲染进程指组件和页面
当我们点了某个按键，触发渲染进程的事件，通过IPC发送给主进程，主进程调用它的事件函数做出应答
顾名思义，IPCMain用于主进程，IPCRenderer用于渲染进程
