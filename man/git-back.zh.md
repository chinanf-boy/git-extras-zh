
# git-back(1)——撤消提交的最新commit

## 简介

`git-back <commitcount>`

## 描述

删除最新提交,并将其更改添加到您的git缓存区域.

## 选项

\<commitcount>

要删除的提交数.默认为 *1*，从而删除最新提交.

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

Kenneth Reitz执笔\<<mailto:me@kennethreitz.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
