
# Git合并回购(1)——合并两个回购历史

## 简介

`git-merge-repo` \<回购协议> \<分支> \<目录> [--壁球]

## 描述

将存储库的历史与当前存储库合并在指定的目录内.

可选的`--squash`标志跳过完整的历史,并仅为合并生成一个提交.

## 实例

合并本地回购协议`frontend`分支到当前回购`web`文件夹:

```
$ git merge-repo ../app/.git frontend web
```

合并远程回购协议`master`分支到当前回购的文件夹:

```
$ git merge-repo git@github.com:tj/git-extras.git master .
```

## 作者

Ivan Malopinsky笔下\<<mailto:hello@imsky.co>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
