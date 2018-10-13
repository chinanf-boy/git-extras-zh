
# Git重命名分支(1)——重命名本地分支并推到远程

## 简介

`git-rename-branch` \<新分行> \<老枝>

## 描述

```
Rename local branch and push the new branch to remote
```

## 选项

```
&lt;new-branch&gt;

New branch name

&lt;old-branch&gt;

Old branch whose has to be renamed. This is an optional parameter. If no value is supplied then the current branch will be renamed.
```

## 实例

```
$ git rename-branch new-name old-name

$ git rename-branch new-name
```

## 作者

Hozefa Jodiawalla执笔\<<mailto:hozefarules@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
