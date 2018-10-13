
# Git标准(1)——回顾提交历史

## 简介

`git-standup` [-作者][-m depth] [d天前][-d date format] [-g][-l] [-f]

`git-standup` -h

## 描述

回想一下你在上一个工作日做了些什么,或者是爱管闲事,找到别人做了什么.

## 选项

\-作者

提交的作者使用"ALL"意味着指定"所有作者".默认为`$(git config user.name)`.

\-m深度

递归目录搜索的深度.默认值为1.

\-L

启用递归目录搜索中的符号链接.

\-d 1

提交历史的开始.默认值为1,意思是"1天前".

D相关

提交历史记录中显示的日期格式.默认为"相对".

\-h

显示帮助消息.

\-g

如果提交是提交消息中的GPG签名(G)或不(N),则显示.

\-f

在提交历史记录之前获取最新的提交.

前一版本`git standup`认可的`<author> <since> <until>`作为选择.这个接口现在被弃用,请避免使用它!

## 实例

这表明您从昨天开始提交:

```
$ git standup

a26d1f9 - add profile hook (69 minutes ago) <spacewander>
```

这显示了作者自上周以来的承诺:

```
$ git standup -a spacewander -d 7

a26d1f9 - add profile hook (70 minutes ago) <spacewander>
4e19859 - fix getTotalSize return value error (6 days ago) <spacewander>
36da84e - fix rename over bound (7 days ago) <spacewander>
8e4182a - add watermark.png (7 days ago) <spacewander>
46fef1d - use tinyXML to configure (7 days ago) <spacewander>
```

如果当前目录不是Git RePO,Git StutUp将从它下面的所有顶级Git RePOS中获取数据:

```
$ cd ..
$ git standup -a spacewander -d 7

someProject/
4e19859 - fix getTotalSize return value error (6 days ago) <spacewander>
36da84e - fix rename over bound (7 days ago) <spacewander>
8e4182a - add watermark.png (7 days ago) <spacewander>
46fef1d - use tinyXML to configure (7 days ago) <spacewander>
```

## 作者

最初来自<https://github.com/kamranahmedse/git-standup>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
