
# Git家务(1)--创建家务琐事

## 简介

`git-chore` [- R -远程\[远程名称\]][finish] \<名称>

## 描述

创建给定的任务分支

## 选项

  \<- R -远程[远程名称_]>

使用远程跟踪分支设置`remote_name`. 如果`remote_name`未提供,使用`origin`默认情况下.

  \<完成>

合并和删除琐碎分支.

  \<名称>

杂货店的名称.

## 实例

```
$ git chore chore-123456
...
$ git commit -m "Some changes"
...
$ git checkout master
$ git chore finish chore-123456

$ git chore -r upstream 123456
```

## 作者

Chris Hall执笔\<<mailto:christopher.k.hall@gmail.com>>由JES埃斯皮诺编写的bug /特征/重构命令\<<mailto:jespinog@gmail.com>>\
Mark Pitman修正\<<mailto:mark.pitman@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
