
# Git别名(1)——定义、搜索和显示别名

## 简介

`git-alias`
`git-alias` \<搜索模式>
`git-alias` \<别名> \<命令>

## 描述

列出所有别名,显示一个别名,或设置一个(全局)别名.

## 选项

  \<搜索模式>

用于搜索别名的模式.

  \<别名>

要创建的别名的名称.

  \<命令>

用于创建别名的命令.

## 实例

定义一个新别名:

```
$ git alias last "cat-file commit HEAD"
```

只提供一个参数,`git-alias`搜索与给定值匹配的别名:

```
$ git alias ^la
last = cat-file commit HEAD
```

 `git-alias`如果不给出任何参数,将显示所有别名:

```
$ git alias
s = status
amend = commit --amend
rank = shortlog -sn --no-merges
whatis = show -s --pretty='tformat:%h (%s, %ad)' --date=short
whois = !sh -c 'git log -i -1 --pretty="format:%an <%ae>
```

## 作者

Jonhnny Weslley笔下\<<mailto:jw@jonhnnyweslley.net>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
