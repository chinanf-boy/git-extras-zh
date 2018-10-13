
# Git失踪(1)-显示从另一个分支丢失

## 简介

`git-missing` [&lt;第一分支&gt;] \<第二分支> [&lt;Git日志选项&gt;]

## 描述

显示在两个分支中的任一个而不是两者中的提交.有助于了解在合并或推送中会遇到什么.

## 选项

  [&lt;第一分支&gt;]

第一个分支进行比较.如果未指定,默认为当前签出的分支.

  \<第二分支>

第二个分支比较.

  [&lt;Git日志选项&gt;]

任何应该传递给Git日志的标志,比如没有合并.

## 实例

显示我的当前分支或硕士,但不是两个:

```
$ git missing master
< d14b8f0 only on current checked out branch
> 97ef387 only on master
```

在分支FO或分支条上显示但不同时提交:

```
$ git missing foo bar
< b8f0d14 only on foo
> f38797e only on bar
```

## 作者

Nate Jones笔下\<<mailto:nate@endot.org>>

## 报告错误

\<<http://github.com/tj/git-extras/issues>>

## 也见

\<<http://github.com/tj/git-extras>>
