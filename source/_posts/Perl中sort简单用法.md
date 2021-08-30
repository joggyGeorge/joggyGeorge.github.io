---
title: Perl中sort简单用法
date: 2021-08-27 14:34:29
tags: Perl
---
Perl中的sort基本格式：
`@sorted = sort {$a cmp $b} @orig;`
或者
`@sorted = sort {$a <=> $b} @orig;`
比较喜欢用cmp

如果倒序则
`@sorted = sort {$b cmp $a} @orig;`

也有进阶用法
不分大小写
`@sorted = sort {fc($a) cmp fc($b)} @orig;`
比较hash的key
`@sorted = sort {$orig{$a} cmp $orig{$b}} keys %orig;`
使用sub函数
``` perl
sub mysub {
    $orig{$a} cmp $orig{$b};
}
@sorted = sort mysub keys %orig;
```
总之可以在cmp左右两边套函数
函数的返回值是-1就\$a放左边，是1就\$b放左边