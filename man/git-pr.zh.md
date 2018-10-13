
# Git PR(1)——在本地检查拉请求

## 简介

`git-pr` \<数> [&lt;遥远的&gt;]<br>
`git-pr` \<网址><br>
`git-pr clean`

## 描述

基于GITHUB拉取请求号或URL创建本地分支,然后切换到该分支.

## 选项

  \<遥远的>

要从中获取的远程名称.默认为`origin`.

  \<网址>

GITHUB拉式请求URL格式`https://github.com/tj/git-extras/pull/453`.

## 实例

这检查拉请求.`226`从`origin`:

```
$ git pr 226

remote: Counting objects: 12, done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 12 (delta 3), reused 9 (delta 3)
Unpacking objects: 100% (12/12), done.
From https://github.com/tj/git-extras
 * [new ref]         refs/pull/226/head -> pr/226

Switched to branch 'pr/226'
```

这是从不同的遥控器拉出来的:

```
$ git pr 226 upstream
```

您还可以基于GITHUB URL签出拉请求:

```
$ git pr https://github.com/tj/git-extras/pull/453

From https://github.com/tj/git-extras
 * [new ref]         refs/pull/453/head -> pr/453
Switched to branch 'pr/453'
```

清理旧树枝:

```
$ git pr clean

Deleted branch pr/226 (was b96a8c2).
Deleted branch pr/220 (was d34dc0f).
```

## 作者

最初来自<https://gist.github.com/gnarf/5406589>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
