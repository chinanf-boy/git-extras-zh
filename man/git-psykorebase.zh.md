
# Git PycRealBasic(1)——用合并提交重新划分一个分支

## 简介

`git-psykorebase` \<目标分支> [\<特征分支>][--no-ff]

`git-psykorebase`--继续

## 描述

重新确立`feature_branch`在上面`target_branch`, the `feature_branch`默认为当前的默认值.

## 选项

  `--no-ff`即使没有冲突也强制提交消息.

  `--continue`在冲突解决后继续保持基地地位.

## 实例

重新设置主分支上的电流分支:

```
$ git psykorebase master --no-ff
```

处理冲突:

```
$ git add README.md
```

继续重播:

```
$ git psykorebase --continue
```

## 作者

由Re'My HubsHER写的\<<mailto:rhubscher@mozilla.com>>

基于贝诺的布赖恩\<<mailto:benoit@marmelune.net>>在Python中实现.

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>

\<<https://github.com/benoitbryon/psykorebase>>
