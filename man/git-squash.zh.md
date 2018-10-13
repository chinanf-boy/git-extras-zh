
# Git SpHASH(1)——从分支导入变化

## 简介

`git-squash` \<源分支> [&lt;提交消息-]

## 描述

生成工作树和索引状态,就像没有提交或合并标记一样发生真正的合并.

## 选项

  \<源分支>

分支在当前分支上挤压.

  \<提交引用>提交引用(必须来自当前分支)也可以用作第一个参数.一系列的约定<sha>头会被压扁.

  \<提交消息>

如果提交消息,提交挤压结果.

## 实例

```
$ git squash my-other-branch
Updating a2740f5..533b19c
Fast-forward
Squash commit -- not updating HEAD
 my-changed-file | 1 +
 1 file changed, 1 insertion(+)
$ git commit -m "New commit without a real merge"

$ git squash HEAD~3 "Commit message"
```

## 作者

杰斯的《埃斯皮诺》\<<mailto:jespinog@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
