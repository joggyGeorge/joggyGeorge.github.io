---
title: POD
date: 2021-08-27 13:30:34
tags: Perl
---
POD: Plain Old Documentations
POD是一种Perl的多行注释方法。
看起来可以用来在代码中编写文档。

格式：
``` perl
=pod 注释
=head1 一级标题
=head2 二级标题
=over 4 缩进空格数为4
=item 项目
=back 结束列表
=begin html 文档设置格式
=end 结束文档设置格式
=cut
```

还可以用pod2html a.pod > b.html来将pod转换为html

注：
感觉有点像这种多行输入，虽然有点不一样。
``` perl
$line = << END;
xxx
xxx
xxx
xxx
END
```

在runoob里叫它Here文档，应该起名不统一。
[runoob](https://www.runoob.com/perl/perl-syntax.html)

1. END后接分号
2. END可替换，保证一致
3. 结束的END自成一行
4. 开始的END不带引号相当于带双引号，带单引号则内容不转义或内嵌（转义: escape; 内嵌: interpolation）
5. 内容有引号不需要转义