
# Git摘要(1)——展示库摘要

## 简介

`git-summary` [线][&lt;commitish&gt;]

## 描述

显示存储库的摘要.

## 选项

  \<共产党员>

仅概述包含在\<共产党员>.

线

用线以外的线来概括.这实际上导致了对`git-line-summary`(1).任何\<共产党员>在指定行时被忽略.见`git-line-summary`(1)更多信息.

## 实例

输出回购协议摘要:

```
$ git summary

project  : express
repo age : 10 months ago
commits  : 1893
active   : 93 days
files    : 111
authors  :
 1285 visionmedia
  478 Tj Holowaychuk
   48 Aaron Heckmann
   34 csausdev
   26 ciaranj
    6 Guillermo Rauch
    3 Nick Poulden
    2 Brian McKinney
    2 Benny Wong
    1 Justin Lilly
    1 James Herdman
    1 Adam Sanderson
    1 Viktor Kelemen
    1 Gregory Ritter
    1 Greg Ritter
    1 ewoudj
    1 isaacs
    1 Matt Colyer
```

这一命令也可以采取公平交易,并将打印一个包含在共产党中的范围的摘要:

```
$ git summary v42..
```

## 作者

Tj Holowaychuk笔下\<<mailto:tj@vision-media.ca>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
