
# Git RePL(1)——Git Read EVE打印环

## 简介

`git-repl`

## 描述

Git读取EVE打印循环.让你奔跑`git`没有键入"Git"的命令.

命令可以用感叹号(前缀)前缀(!)被解释为常规命令.

类型`exit`或`quit`结束RePL会话.

## 命令

  \<命令>

解释为`git <command>`.

!\<命令>

解释为`<command>`(未通过`git`)

  ls

相当于"Git LS文件".

退出退出

结束RePL会话.

## 实例

```
$ git repl
git version 2.9.2
git-extras version 3.0.0
type 'ls' to ls files below current directory,
'!command' to execute any command or just 'subcommand' to execute any git subcommand

git (master)> ls-files
History.md
Makefile
Readme.md
bin/git-changelog
bin/git-count
bin/git-delete-branch
bin/git-delete-tag
bin/git-ignore
bin/git-release

git (master)> !echo Straight from the shell!
Straight from the shell!

git (master)> quit
```

## 作者

Tj Holowaychuk执笔\<<mailto:tj@vision-media.ca>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
