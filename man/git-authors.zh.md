
# git-authors(1)——生成关于作者们的报告

## 简介

`git-authors [-l,-list] [--no-email]`

## 描述

匹配`authors|contributors -i`和提交的作者，再根据每位作者的提交数量.

用`$EDITOR`打开文件，若设置了

见**git-shortlog**(1)的["MAPPING AUTHORS" 章节](http://git-scm.com/docs/git-shortlog#_mapping_authors),统计同一个人的提交.

## 选项

-l, --list

展示作者.

--no-email

不要显示作者的电子邮件.

## 实例

-   可更新作者文件:

```
    $ git authors
```

-   列表作者:

```
    $ git authors --list
```

```
TJ Holowaychuk <tj@vision-media.ca>
hemanth.hm <hemanth.hm@gmail.com>
Jonhnny Weslley <jw@jonhnnyweslley.net>
nickl- <github@jigsoft.co.za>
Leila Muhtasib <muhtasib@gmail.com>
```

-   列出没有电子邮件的作者:

```
    $ git authors --list --no-email
```       

```
TJ Holowaychuk
hemanth.hm
Jonhnny Weslley
nickl-
Leila Muhtasib
```

## 作者

Titus Wormer执笔\<<mailto:tituswormer@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
