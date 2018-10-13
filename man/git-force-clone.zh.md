
# Git强制克隆(1)——用克隆覆盖本地存储库

## 简介

`force-clone --help`
`force-clone {remote_url} {destination_path}`
`force-clone --branch {branch_name} {remote_url} {destination_path}`

## 描述

提供基本功能`git clone`但是,如果目的地Git存储库已经存在,它将强制重置它类似于远程克隆.

因为它实际上并没有删除目录,所以它通常比删除目录和从零开始克隆存储库的速度快得多.

**注意安全**如果存储库存在,这将破坏*全部的*本地工作:更改文件将被重置,本地分支和其他远程将被删除.

## 过程

如果`target-directory`不存在或不是Git存储库,那么参数将被简单地传递给`git clone`.

如果`target-directory`存在并且是一个Git存储库,然后将:

-   删除所有遥控器
-   将原点远程设置为`{remote_url}`把遥控器拿来
-   如果没有指定分支,则发现默认分支
-   选中选定的分支
-   删除所有其他本地分支

## 选项

`{remote_url}`-一个Git远程存储库的URL,用于创建克隆.`{destination_path}`-到本地GIT存储库位置的路径克隆.`--branch {branch_name}`克隆后,检查这个分支.

## 实例

`git-force-clone -b master git@github.com:me/repo.git ./repo_dir`

## 作者

Robin Winslow笔下<mailto:robin@robinwinslow.co.uk>.

## 报告错误

<https://github.com/tj/git-extras/issues>

## 也见

<https://github.com/tj/git-extras>
