
# Git忽略IO(1)-获取示例GiTigGORE文件

## 简介

`git ignore-io` [&lt;选项&gt;]

## 描述

获取示例GiTigGORE文件[gitignore.io](https://www.gitignore.io)

## 选项

  \<选项>

\-A,-追加\<类型>…\
在当前目录下将新的GiTigNoR内容追加到GiTigGORE

\-R,-替换\<类型>…\
将新的GiTigGORE导出到当前目录(旧的目录将被替换)

\-列表中的列表\
以表格格式打印可用的类型

\-L,按字母顺序排列\
按字母顺序打印可用的类型

\-S,-搜索\<单词>\
可用类型搜索单词

\-t,显示更新时间\
显示~//GI的最后修改时间γ列表(其中存储可用类型的列表)

\-更新列表\
更新~/γ列表

## 实例

为VIM显示示例GiTigGORE文件

```bash
$ git ignore-io vim

    # Created by https://www.gitignore.io/api/vim

    ### Vim ###
    [._]*.s[a-w][a-z]
    [._]s[a-w][a-z]
    *.un~
    Session.vim
    .netrwhist
    *~
```

在当前目录中为VIM和Python添加GiTimGORE到GiTigGORE.

```bash
$ git ignore-io -a vim python
```

显示所有可用类型

```bash
$ git ignore-io -l

    actionscript             ada                      agda                     android                  anjuta
    appceleratortitanium     appcode                  appengine                archives                 archlinuxpackages
    autotools                basercms                 bazel                    bluej                    bower
    bricxcc                  c                        c++                      cakephp                  carthage
    ......
```

在所有可用类型中搜索JA

```bash
$ git ignore-io -s ja

    django
    jabref
    java
    ninja
```

## 作者

刘易文<mailto:cl87654321@gmail.com> 

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
