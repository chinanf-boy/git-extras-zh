
# Git拉动请求(1)——为GITHUB项目创建拉动请求

## 简介

`git-pull-request` [&lt;目标分支&gt;]

## 描述

通过命令行在GITHUB上创建项目的拉动请求.

使用电子邮件来自`git config user.email`打开拉取请求.

## 选项

\<目标分支>

要发送请求的目标分支到.

## 实例

```
$ git pull-request master
Everything up-to-date

  create pull-request for spacewander/spacewander-toolbox 'master'

  title: test
  body:  
  base [master]: 
  GitHub two-factor authentication code (leave blank if not set up): 

Enter host password for user 'spacewanderlzx@gmail.com':
...
```

## 作者

Tj Holowaychuk笔下\<<mailto:tj@vision-media.ca>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
