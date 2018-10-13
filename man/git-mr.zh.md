
# GIT MR(1)——检查本地合并请求

## 简介

`git-mr` \<数> [&lt;遥远的&gt;]<br>
`git-mr` \<网址><br>
`git-mr clean`

## 描述

以其编号或URL获取合并请求头,并在合并请求号命名的分支中检查它.

## 选项

  \<遥远的>

要从中获取的远程名称.默认为`origin`.

  \<网址>

GITLAB合并请求URL格式`https://gitlab.tld/owner/repository/merge_requests/453`.

## 实例

这检查合并请求.`!51`从遥远`origin`支流`mr/51`.

```
$ git mr 51
From gitlab.com:owner/repository
 * [new ref]         refs/merge-requests/51/head -> mr/51
Switched to branch 'mr/51'
```

## 作者

由爱迪丝贝尔萨克撰稿<mailto:bersace03@gmail.com>来自GIT PR(1).

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
