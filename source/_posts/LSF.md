---
title: LSF
date: 2021-10-15 22:33:45
tags: 
---
LSF是一个作业管理系统，应该是IBM的。公司里用它来提交仿真任务。
bhosts 得出节点列表
bqueues 得出队列列表
bjobs 得出任务列表
bsub -n CPU数 -q 队列名 -i input -o output 指令
指令可以是bash指令也可以是包含指令的程序
bjobs -l JOBID job详细信息
bkill 终止任务
bpeek 查看任务输出
bhist 得出作业历史
bparams 得出配置参数
bstop 暂停任务
bresume 恢复任务

lsload 查看节点负载
lsid 查看LSF信息
