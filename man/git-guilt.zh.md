
# Git罪(1)——计算两次修订之间的变化

## 简介

`git guilt` [&lt;选项&gt;]<br>
`git guilt` [&lt;选项&gt;] \<自从> [&lt;直到&gt;]

## 描述

在第一种形式中,显示了具有未分级变更的文件的总指责计数.

在第二种形式中,计算两个修订之间的错误变化.如果未指定,\<直到>将默认为头部.

## 选项

  \-h

输出使用信息

\-电子邮件

显示作者的电子邮件而不是姓名

\-W,-忽略空白

仅在归因错误时忽略空白

\-D,-Debug

输出调试信息

## 实例

发现未经修改的文件归咎于:

```
$ git guilt      (1)
spacewander                   ++++

(1) There is only one modified file and it is not staged. The four
pluses means that the file has four lines, all contributed by spacewander.
```

发现两个提交之间的责任三角:

```
$ git guilt HEAD~3 HEAD^
spacewander                   +++++++++++++++++++++++++++++++++++++++++++++(115)
Jesse Sipprell                -
```

在过去的三个星期里发现责任三角洲:

```
$ git guilt `git log --until="3 weeks ago" --format="%H" -n 1`
Paul Schreiber                +++++++++++++++++++++++++++++++++++++++++++++(349)
spacewander                   +++++++++++++++++++++++++++++++++++++++++++++(113)
Mark Eissler                  ++++++++++++++++++++++++++
CJ                            +++++
nickl-                        -
Jesse Sipprell                -
Evan Grim                     -
Ben Parnell                   -
hemanth.hm                    --
```

由于GIT 1.85,上述也可以写成:

$Git疚@ { 3周前}

寻找一个主题分支:

```
$ git guilt `git merge-base master git-guilt` git-guilt 
spacewander                   +++++++++++++++++++++++++++++++++++++++++++++(112)
```

## 作者

太空漫游者\<<mailto:spacewanderlzx@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
