
# Git重命名标签(1)——重命名标签

## 简介

`git-rename-tag` \<旧标签名> \<新标签名>

## 描述

重命名标签(本地和远程)

## 选项

  \<旧标签名>

要重命名的标记的名称.

  \<新标签名>

标签的新名称.

## 实例

```
$ git tag test
$ git push --tags
Total 0 (delta 0), reused 0 (delta 0)
To git@myserver.com:myuser/myrepository.git
 * [new tag]         test -> test
$ git tag
test
$ git rename-tag test test2
Deleted tag 'test' (was 1111111)
Total 0 (delta 0), reused 0 (delta 0)
To git@myserver.com:myuser/myrepository.git
 * [new tag]         test2 -> test2
remote: warning: Deleting a non-existent ref.
To git@myserver.com:myuser/myrepository.git
 - [deleted]         refs/tag/test
$ git tag
test2
```

## 作者

杰斯的《埃斯皮诺》\<<mailto:jespinog@gmail.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
