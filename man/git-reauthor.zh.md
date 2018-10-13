
# GIT改写者(1)——改写历史改变作者身份

## 简介

`git reauthor [<options>]`

## 描述

允许您在提交和标记中替换作者和/或提交者身份.

该命令遍历所有本地分支中的所有现有提交和标记,以选择性地修改这些对象中存在的标识.所有其他信息,如日期,消息,…被保存下来.

可以使用--all标志重写提交和标记对象中的所有标识,或者只替换电子邮件与--old-email选项的值匹配的标识.还可以将重写限制为某种类型的身份:作者或提交者身份.默认情况下,它们都受到影响.\
对于要更新的每个标识,命令将使用通过选项定义的新正确值替换名称和/或电子邮件.如果未定义新的身份名称,则当前的名称将被保留(反之亦然).

`WARNING!`这个命令重写历史,因此如果不使用--force选项,您将无法将分支推到远程.\
查看更多信息`git help filter-branch`.

## 选项

\-A,所有

```
Rewrite ALL identities in commits and tags.
```

\-C,-使用配置

```
Define correct values from user Git config
Values of --correct-email and --correct-name options take precedence over the ones from the config if specified as well
```

\-正确的电子邮件\<<email>>

```
Define the correct email to set
Empty email '' is allowed
```

\-n,-更正名称\<<name>>

```
Define the correct name to set
Empty name '' is not allowed
```

o,旧电子邮件\<<email>>

```
Rewrite identities matching old email in commits and tags
Empty email '' is allowed
```

\-T型\<<id>>

```
Define the type of identities affected by the rewrite
Possible type identifiers are: author, committer, both (default)
```

## 实例

将个人电子邮件和杰克的名字替换为他的工作

```
$ git reauthor --old-email jack@perso.me --correct-email jack@work.com --correct-name 'Jack Foobar'
```

将电子邮件和杰克的名称替换为Git配置中定义的电子邮件

```
$ git reauthor --old-email jack@perso.me --use-config
```

仅替换杰克的电子邮件(保留已使用的名称)

```
$ git reauthor --old-email jack@perso --correct-email jack@perso.me
```

只更改杰克的提交邮件(保留作者已使用的电子邮件)

```
$ git reauthor --old-email jack@perso.me --correct-email jack@work.com --type committer
```

将杰克的身份设置为整个存储库中的唯一一个

```
$ git reauthor --all --correct-email jack@perso.me --correct-name Jack
```

将杰克设置为整个存储库的唯一提交器(保持作者)

```
$ git reauthor --all --correct-email jack@perso.me --correct-name Jack --type committer
```

## 作者

Damien Tardy Panis执笔\<<mailto:damien@tardypad.me>>

## 报告错误

\<<http://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
