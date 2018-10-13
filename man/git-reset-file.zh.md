
# Git重置文件(1)-重置一个文件

## 简介

`git-reset-file` [&lt;文件名&gt;]提交哈希

## 描述

将一个文件重置为头或某些提交哈希

## 选项

  \<文件名>

要重置的文件的名称.

  \<提交哈希>

(可选)将文件重置为提交的哈希.默认为头.

## 实例

重置一文件到头

```
$ git reset-file .htaccess
```

或将一个文件重置为某些提交

```
$ git reset-file .htaccess dc82b19
```

## 作者

Sasha Khamkov笔下\<<mailto:sanusart@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
