
# Git Trimib(1)——展示用户的贡献

## 简介

`git-contrib` [&lt;用户名&gt;|&lt;γ&gt;电子邮件]

## 描述

基于作者姓名或电子邮件输出用户对项目的贡献.如果有多个匹配项,则返回多个条目.

## 选项

  \<用户名>

拥有捐款的用户的姓名或电子邮件.

## 实例

```
Searching with a username

$ git contrib visionmedia
visionmedia (18):
  Export STATUS_CODES
  Moved help msg to node-repl
  Added multiple arg support for sys.puts(), print(), etc.
  Fix stack output on socket error
  ...

Searching with a partial email

$ git contrib tj@
visionmedia (18):
  Export STATUS_CODES
  Moved help msg to node-repl
  Added multiple arg support for sys.puts(), print(), etc.
  Fix stack output on socket error
  ...
```

## 作者

Tj Holowaychuk执笔\<<mailto:tj@vision-media.ca>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
