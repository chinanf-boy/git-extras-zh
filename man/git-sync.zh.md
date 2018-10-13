
# Git同步(1)——同步本地分支与远程分支

## 简介

  `git sync` [ &lt;遥远的&gt; &lt;分支&gt; ]

## 描述

同步本地分支\<遥远的>/\<分支>.

什么时候?\<遥远的>和\<分支>在命令行上未指定,默认情况下将使用本地分支的上游.

所有的更改和未跟踪的文件和目录都将被删除.

## 实例

同步本地分支及其上游

```
$ git sync
```

与源/主同步同步本地分支

```
$ git sync origin master
```

## 作者

Takuma Yamaguchi笔下\<<mailto:kumon0587@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
