
# git-bug(1)——创建bug分支

## 简介

`git-bug` **[-r|--remote [remote_name]] [finish] &lt;name&gt;**

## 描述

创建给定的错误分支

## 选项

\<-r|--remote [remote_name]>

使用远程跟踪分支设置`remote_name`. 如果`remote_name`未提供,默认情况下使用`origin`.

\<finish>

合并并删除bug分支.

\<name>

错误分支的名称.

## 实例

```
$ git bug bug-123456
...
$ git commit -m "Some changes"
...
$ git checkout master
$ git bug finish bug-123456

$ git bug -r 12345
```

## 作者

Jesús Espino执笔\<<mailto:jespinog@gmail.com>>\
Mark Pitman修正\<<mailto:mark.pitman@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
