
# Git戳(1)——戳最后提交消息

## 简介

`git stamp [<options>] <id> [<messages>]`

## 描述

让您用邮票消息修改最后提交.

命令将其标识符的消息追加到最后提交消息.\
默认情况下,所有的邮票都被附加到提交消息的新段落中.\
可以通过使用替换标志来改变这种行为.\
有了这个标志,所有的具有相同标识符的相关邮票将首先被删除,然后再添加新的标识符.

`WARNING!`如果没有邮票的提交消息有一个从同一标识符开头的行,它将被解释为一个戳.

## 选项

\-R,-替换

```
Replace all previous stamps in the last commit message that have the same identifier  
The identifier is case insensitive for this replacement
```

## 实例

提交消息是

```
| Fix timezone bug
```

引用来自bug跟踪程序的问题号

```
$ git stamp Issue FOO-123
$ git stamp Issue FOO-456 \#close

| Fix timezone bug
|
| Issue FOO-123
|
| Issue FOO-456 #close
```

链接到它的评论页面

```
$ git stamp Review https://reviews.foo.org/r/4567/

| Fix timezone bug
|
| Issue FOO-123
|
| Issue FOO-456 #close
|
| Review https://reviews.foo.org/r/4567/
```

用新的问题替换以前的问题\
(注意标识符不区分大小写)

```
$ git stamp --replace issue BAR-123

| Fix timezone bug
|
| Review https://reviews.foo.org/r/4567/
|
| issue BAR-123
```

## 作者

Damien Tardy Panis笔下\<<mailto:damien@tardypad.me>>

## 报告错误

\<<http://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
