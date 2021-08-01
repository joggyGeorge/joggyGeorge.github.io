---
title: React中使用css style
date: 2021-08-01 18:30:00
tags: React CSS
---
React里的组件使用css style有一些语法上的不同，例如不能使用-划线，一般是驼峰命名法，即首字母小写后面大写
用两个大括号括起来，不同属性之间用,逗号隔开，属性名不用引号，但属性值需要引号
例：
```javascript
style={{borderRadius: '10px'}}
