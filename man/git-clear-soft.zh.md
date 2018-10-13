
# GIT清除软(1)-软清理储存库

## 简介

`git-clear-soft`

## 描述

将存储库清除到它看起来像是用当前HEAD新克隆的状态,但是,保留位于.gitignore中列出的文件和目录中的所有更改.它是一个git-reset——与删除所有驻留在工作目录内的未跟踪文件一起很难,不包括.gitignore中的那些文件.

## 实例

清除回购协议.

```
$ git clear-soft
```

## 作者

丹尼尔《格林德》的剧本改编版\<<mailto:grindhold@gmx.net>>Matiss Treinis\<<mailto:mrtreinis@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
