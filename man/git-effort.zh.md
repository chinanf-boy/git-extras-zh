
# Git努力(1)——显示文件上的努力统计信息

## 简介

`git-effort` [--以上\<价值>][&lt;path&gt;...]\[[&lt;日志选项&gt;...…]]

## 描述

显示存储库中有关文件的努力统计.

显示包括:

-   提交:每个文件的提交数量-突出显示最多活动的文件.
-   活动天数:对该文件进行修改的总天数.

## 选项

\--以上\<价值>

用文件忽略文件\<=一个值.

  \<路径>…

只计算触碰给定路径的提交.

注:`git-effort`不接受修订范围,但基础`git log`(看例子).

  \<日志选项>…

选项`git log`. 注意,必须使用`--`将选项分开`git log`从选项到`git effort`.   这使得你可以只计算你感兴趣的承诺.并非所有选项都与上下文相关`git-effort`但是那些是在"提交限制"部分上列出的.`git-log`手册.

## 实例

注意:输出将首先出现未排序,然后屏幕被清除并且排序列表被输出.在简短的例子中未显示初始未排序列表.

显示"努力"统计:

```
$ git effort --above 5

  file                                          commits    active days

  git-extras                                    26         18
  git-release                                   13         13
  git-effort                                    13         2
  git-ignore                                    11         7
  git-changelog                                 11         8
  git-graft                                     9          6
  git-summary                                   8          6
  git-delete-branch                             8          6
  git-repl                                      7          5


$ git effort --above 5 bin/* -- --after="one year ago" --author="Leila Muhtasib"

  file                                          commits    active days

  git-extras                                    15         12
  git-release                                   6          4
  git-effort                                    6          2
  git-ignore                                    4          4
  git-changelog                                 3          2
  git-graft                                     2          2
```

显示目录的统计数据也是可能的:

```
$ git effort bin man -- --after="one year ago"

  file                                          commits    active days

  bin.......................................... 406        232
  man.......................................... 118        80
```

只计算指定修订范围内的提交:

$GIT努力-大师…

```
  file                                          commits    active days

  bin/git-effort............................... 3          2
  man/git-effort.md............................ 1          1
```

## 作者

Leila Muhtasib执笔\<<mailto:muhtasib@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
