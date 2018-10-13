
# Git信息(1)——返回当前存储库的信息

## 简介

`git-info`

## 描述

显示有关存储库的下列信息:

1.  远程URL(S)
2.  远程分支
3.  当地分支机构
4.  最近提交
5.  配置信息

## 选项

不适用

## 实例

关于回购的信息输出:

```
$ git info

## Remote URLs:

origin		git@github.com:sampleAuthor/git-extras.git (fetch)
origin		git@github.com:sampleAuthor/git-extras.git (push)

## Remote Branches:

origin/HEAD -> origin/master
origin/myBranch

## Local Branches:

myBranch
* master

## Most Recent Commit:

commit e3952df2c172c6f3eb533d8d0b1a6c77250769a7
Author: Sample Author <sampleAuthor@gmail.com>

Added git-info command.

Type 'git log' for more commits, or 'git show <commit id>' for full commit details.

## Configuration (.git/config):

color.diff=auto
color.status=auto
color.branch=auto
user.name=Sample Author
user.email=sampleAuthor@gmail.com
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
remote.origin.url=git@github.com:mub/git-extras.git
branch.master.remote=origin
branch.master.merge=refs/heads/master
```

## 作者

Leila Muhtasib笔下\<<mailto:muhtasib@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
