
# Git提交自(1)——显示某个日期以来的提交日志

## 简介

`git-commits-since` [&lt;日期&gt;]

## 描述

自提交以来的提交列表*日期*.

## 选项

  \<日期>

显示比最近提交更多<date>. 默认情况下,命令从"上周"显示提交日志.

## 实例

这是非常灵活的,这些只是3个选项,继续尝试一下:

```
$ git commits-since yesterday
... commits since yesterday
nickl- - Merge branch upstream master.
nickl- - Rebase bolshakov with master
TJ Holowaychuk - Merge pull request #128 from nickl-/git-extras-html-hyperlinks
TJ Holowaychuk - Merge pull request #129 from nickl-/develop
nickl- - Fix #127 git-ignore won't add duplicates.

$ git commits-since 3 o clock pm
... commits since 3 o clock pm
nickl- - Merge branch upstream master.

$ git commits-since 2 hour ago
... commits since 2 hour ago
nickl- - Merge branch upstream master.
TJ Holowaychuk - Merge pull request #128 from nickl-/git-extras-html-hyperlinks
TJ Holowaychuk - Merge pull request #129 from nickl-/develop
```

## 作者

Tj Holowaychuk执笔\<<mailto:tj@vision-media.ca>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
