
# git湮没(1)-重写过去提交删除文件

## 简介

擦除\<文件夹...> [——--Rev列表选项…&lt;]

## 描述

完全删除存储库中的一些文件,包括过去的提交和标签.警告!此命令将重写历史,类似于`git rebase`(虽然影响更大).重写历史将有不同的对象名称,所有的对象,将不会收敛与原来的分支.所以**避免在共享的提交上使用它**. 它会把垃圾藏起来,所以**当你跑的时候不要有垃圾`git obliterate`**.

## 选项

您可以通过Rev列表选项来指示受影响的范围.这些选项需要在它们之前与"-----"分开.跑`git help rev-list`查看可接受的选项.

## 实例

从存储库中删除秘密:

```
$ git obliterate .secret
```

从原点和特征之间删除秘密:

```
$ git obliterate .secret -- feature ^origin
```

从提交ABCDEFG到提交1234567的秘密

```
$ git obliterate .secret -- abcdefg..1234567
```

## 作者

由书面\<<mailto:brianloveswords@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
