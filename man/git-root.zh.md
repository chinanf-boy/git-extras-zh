
# Git根(1)——根的显示路径

## 简介

`git root` [选项]

## 描述

打印Git RePo根目录的路径

## 选项

\-R,相对

显示从根目录到当前目录的相对路径

## 实例

```
$ cd .../git-extras/bin
$ git root -r
bin/
$ git root
/home/.../git-extras
$ cd `git root`
$ pwd
/home/.../git-extras
# then we can
$ git add . && git commit
```

## 作者

太空漫游者\<<mailto:spacewanderlzx@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
