
# Git delta(1)——列出已更改的文件

## 简介

`git-delta` [\<分支>][&lt;filter&gt;]

## 描述

列出与分支不同的所有文件.默认情况下,与已添加、复制或修改的列表文件相比,`master`分支机构.

## 实例

列出所有已修改和重命名的文件vs.`master`:

```
$ git delta master MR
```

列出所有删除的文件vs.`example`:

```
$ git delta example D
```

## 作者

Ivan Malopinsky笔下\<<mailto:hello@imsky.co>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
