
# Git SCP(1)——将文件复制到SSH兼容`git-remote`

## 简介

```
`git scp` -h|help|?
`git scp` <remote> [<commits>...|<path>...]
`git rscp` <remote> <path>
```

## 描述

将文件从当前工作树复制到远程存储库的工作目录的简便方法.如果A`<commits>...`只提供在提交范围内更改的文件将被复制.

内部脚本使用`rsync`而不是`scp`顾名思义.

`git-rscp`-相反的`git-scp`. 将特定文件从远程存储库的工作目录复制到当前工作目录.

## 选项

  \<遥远的>

```
The git remote where you want to copy your files.
```

  \<提交>…

```
Any commit, commit range or tree. Uses `git-diff`(1)
```

  \<路径>…

```
The <paths> parameters, when given, are used to limit the diff to the named paths (you can give directory names and get diff for all files under them).
```

## Git组态

使用文件消毒`dos2unix`复制文件之前

```
$ git config --global --add extras.scp.sanitize dos2unix
```

可以通过PHPLIN运行文件(即`php -l`)在复制文件之前

```
$ git config --global --add extras.scp.sanitize php_lint
```

## 实例

确保你有`git-remote`(1)设置

```
$ git remote add staging myStagingServer:/var/www/html
```

将未分级文件复制到远程.当你想做快速测试而不做任何承诺时

```
$ git scp staging
```

将阶段和未分级文件复制到远程

```
$ git scp staging HEAD
```

复制上次提交中已更改的文件,再将任何阶段性或未分级文件复制到远程

```
$ git scp staging HEAD~1
```

复制在现在和标签之间更改的文件

```
$ git scp staging v1.2.3
```

复制特定文件

```
$ git scp staging index.html .gitignore .htaccess
```

复制特定目录

```
$ git scp staging js/vendor/
```

将文件从特定目录复制到多个服务器

```
$ for dest in web1 web2 web3; do
    git diff --name-only 4.8.3 4.8.2 app/code/community app/design skin/ | xargs git scp $dest
done;
```

## 作者

Chern Jie执笔\<<mailto:lim@chernjie.com>>

## 报告错误

\<<https://github.com/chernjie/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
