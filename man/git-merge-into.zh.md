
# Git合并成(1)——合并一个分支到另一个分支

## 简介

`git merge-into` [src] \<最> [——仅FF--]

## 描述

将一个分支合并到另一个分支中,并保持在当前分支上.如果没有给出SRC分支,它将合并当前一个到DEST.

## 选项

  \<src>

分支的名称将合并为.如果没有给出,则使用当前分支作为默认值.

  \<最>

要合并的分支的名称.

——仅FF

拒绝合并并以非零状态退出,除非当前HEAD已经是最新的,或者合并可以快速解决.

## 实例

假设存在以下历史,当前分支为SRC:

```
                 A---B---C src(current)
                /
           D---E---F---G dest
```

运行后`git merge-into dest`看起来会像这样:

```
                A---B---C src(current)
                /         \
           D---E---F---G---H dest
```

这个`H`提交将记录合并结果,就像什么一样`git merge`做.和`src`还是目前的分支机构.

默认实现`merge-into`使用`git checkout`和`git merge`这可能会导致工作树发生暂时性的变化.如果确保分支可以快速向前合并,请添加`--ff-only`避免文件更改.

## 作者

太空漫游者\<<mailto:spacewanderlzx@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
