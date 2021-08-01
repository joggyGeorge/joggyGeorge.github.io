---
title: Execution policy
date: 2021-08-01 18:30:00
tags: Windows
---
这个在安装软件的时候都会碰到，防止不信任的脚本擅自修改电脑
[Microsoft Doc](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7.1)
有几种设置：
- Restricted 最常见的，不允许
- AllSigned 所有都必须签名，包括自己写的
- Bypass 允许
- Default 默认，主机是Restricted，服务器是Remote-Signed
- Remote-Signed 下载的必须签名
- Undefined 未定（依赖别的权限）
- Unrestricted 没签名的会提示
