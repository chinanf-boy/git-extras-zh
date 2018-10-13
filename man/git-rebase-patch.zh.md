
# Git垫底-(1)- rebases补丁补丁

## 简介

`git-rebase-patch` \<补丁文件>

## 描述

你有一个给定的补丁是不是适用于目前的头,但你知道它的一些应用.在过去,`git-rebase-patch`这将帮助你找到的交付和定位.

## 期权

-   \<补丁文件>在补丁被应用.

## 实例

自动执行

```
$ git rebase-patch test.patch
```

像那样的东西可以给你.

```
Trying to find a commit the patch applies to...
Patch applied to dbcf408dd26 as 7dc8b23ae1a
First, rewinding head to replay your work on top of it...
Applying: test.patch
Using index info to reconstruct a base tree...
Falling back to patching base and 3-way merge...
Auto-merging README.txt
```

然后你的最后提交的变化,蛛网膜下腔出血(SAH)的补丁是——*test.patch*.......

## 作者

书面由Niklas fiekas\<<mailto:niklas.fiekas@tu-clausthal.de>>

## 报告的bug

\<<http://github.com/tj/git-extras/issues>>

## 国有企业也

\<<http://github.com/tj/git-extras>>
