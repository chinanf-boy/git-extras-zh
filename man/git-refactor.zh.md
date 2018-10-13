
# Git重构(1)——创建重构分支

## 简介

`git-refactor` [- R -远程\[远程名称\]][finish] \<名称>

## 描述

创建给定的重构分支

## 选项

  \<- R -远程[远程名称_]>

使用远程跟踪分支设置`remote_name`. 如果`remote_name`未提供,使用`origin`默认情况下.

  \<完成>

合并并删除重构分支.

  \<名称>

重构分支的名称.

## 实例

```
$ git refactor mainlib_refactor
...
$ git commit -m "Some changes"
...
$ git checkout master
$ git refactor finish mainlib_refactor

$ $ git refactor -r upstream mainlib_refactor
```

## 作者

杰斯的《埃斯皮诺》\<<mailto:jespinog@gmail.com>>\
Mark Pitman修正\<<mailto:mark.pitman@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
