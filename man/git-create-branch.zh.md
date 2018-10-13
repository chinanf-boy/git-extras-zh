
# Git创建分支(1)——创建分支

## 简介

`git-create-branch`\[R-远程][远程名称_]] \<鳃鲨>

## 描述

创建本地分支命名\<鳃鲨>并可选地设置远程跟踪分支.

## 选项

  \<- R -远程[远程名称_]>

使用远程跟踪分支设置`remote_name`. 如果`remote_name`未提供,使用`origin`默认情况下.

  \<鳃鲨>

要创建的分支的名称.

## 实例

```
$ git create-branch integration

$ git create-branch -r integration

$ git create-branch -r upstream integration
```

## 笔记

在4.4.0中,默认行为发生了变化.`git-create-branch`将不再自动设置远程跟踪分支,除非`-r|-remote`选项被指定.

## 作者

Jonhnny Weslley执笔\<<mailto:jw@jonhnnyweslley.net>>\
Mark Pitman修正\<<mailto:mark.pitman@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
