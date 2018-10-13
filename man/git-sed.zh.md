
# Git See(1)——Git受控文件中的模式替换

## 简介

`git-sed` [ -c ][ -f <flags> ] <search> <replacement> [ <flags> ]

## 描述

运行git grep,然后将结果发送到sed以便用给定的标志替换,如果它们是通过-f提供的,或者作为第三个参数提供的.

还提供了Git提交IF -C.

## 选项

  \-c

用标准提交消息提交最终的更改,详细说明确切的命令RAN.如果有未更改的更改,将失败.

  \<旗帜>   -f \<旗帜>

将使用SED命令中的给定正则表达式标志(例如"G")在同一行上替换多次.

  \<搜索>

该模式传递给GRIP和SED表达式的第一部分.

  \<替换>

替换传递给SED,SED表达式的第二部分.

## 实例

```
$ git sed 'my_function' 'do_stuff'
# ... only does the changes, without committing
$ git commit -m"use proper function name"
$ git sed -c 'do_stuff' 'stuff'
# .. does the changes and a commit
$ git sed -f g do_stuff stuff
# .. g is actually pretty important, otherwise you will miss some
# stuff!
```

## 作者

安托万\<<mailto:anarcat@debian.org>>灵感来自<https://github.com/da-x/git-search-replace>和<http://stackoverflow.com/questions/9651898/is-there-a-git-sed-or-equivalent>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
