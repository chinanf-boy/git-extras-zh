
# Git后退(1)——撤消并提交最新提交

## 简介

`git-back` [&lt;委托计数&gt;]

## 描述

删除最新提交,并将其更改添加到您的分级区域.

## 选项

  \<委托计数>

要删除的提交数.默认为*一*从而删除最新提交.

## 实例

移除最新提交.

```
$ git back
```

删除最近3个提交:

```
$ git back 3
```

## 作者

Kenneth Reitz笔下\<<mailto:me@kennethreitz.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
