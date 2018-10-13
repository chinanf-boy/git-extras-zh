
# Git特征(1)——创建/合并特征分支

## 简介

`git-feature` [- |--别名分支前缀_]- R -远程[远程名称_]] [完成] \<名称>

## 描述

创建/合并给定的特征分支

## 选项

  \<-\* -别名分支前缀>

使用`branch_prefix`而不是`feature`

  \<- R -远程[远程名称_]>

使用远程跟踪分支设置`remote_name`. 如果`remote_name`未提供,使用`origin`默认情况下.

  \<完成>

合并并删除特征分支.

  \<名称>

特征分支的名称.

## 实例

```
$ git feature dependencies
...
$ (feature/dependencies) git commit -m "Some changes"
...
$ (feature/dependencies) git checkout master
$ git feature finish dependencies

$ git alias features "feature -a features"
$ git features dependencies
$ (features/dependencies) ...
$ (features/dependencies) git checkout master
$ git features finish dependencies

$ git feature dependencies -r upstream
```

## 作者

杰斯的《埃斯皮诺》\<<mailto:jespinog@gmail.com>>\
Mark Pitman修正\<<mailto:mark.pitman@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
