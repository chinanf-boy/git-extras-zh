
# Git撤消(1)-删除最新提交

## 简介

`git-undo` [\<委托计数>][-s, --soft, -h, --hard]

## 描述

移除最新提交.

## 选项

\--软或-S

这是默认的,只会回滚提交,但更改仍然未完成.

\--硬还是-H

此选项擦除您的提交,从而无法恢复您的更改.小心使用.避免混淆`--help`将在何时确认`-h`指定.

  \<委托计数>

要删除的提交数.默认为*一*从而删除最新提交.

## 实例

移除最新提交.

```
$ git undo
```

删除最近3个提交:

```
$ git undo 3
```

## 作者

Kenneth Reitz笔下\<<mailto:me@kennethreitz.com>>Nick Lombard\<<mailto:github@jigsoft.co.za>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
