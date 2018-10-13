
# Git叉(1)——叉上GITHUB的回购协议

## 简介

`git-fork` [&lt;GITHUB回购协议URL-]

## 描述

如果给出了GITHUB回购协议URL,请叉回回购协议.像克隆,但叉子第一.

1.  在Github上进行回购
2.  将回购协议克隆到当前DIR中
3.  将原始回购作为远程调用`upstream`

    如果没有给出URL,当前DIR是GITHUB回购,叉回购.

4.  分叉当前回购
5.  重命名`origin`远程回购`upstream`
6.  将叉式回购作为远程调用`origin`

    Relots将使用SSH,如果您使用GITHUB配置它,如果没有,HTTPS将被使用.

## 例子

叉期望

```
$ git fork https://github.com/LearnBoost/expect.js
```

或者只是:

```
$ git fork LearnBoost/expect.js
```

然后:

```
$ ..<forks into your github profile and clones repo locally to expect.js dir>...

$ cd expect.js && git remote -v

  origin          git@github.com:<user>/expect.js (fetch)
  origin          git@github.com:<user>/expect.js (push)
  upstream        git@github.com:LearnBoost/expect.js (fetch)
  upstream        git@github.com:LearnBoost/expect.js (push)
```

如果当前DIR是预期的J.js的克隆,则具有相同的效果:

```
$ git fork
```

## 作者

Andrew Griffiths笔下\<<mailto:mail@andrewgriffithsonline.com>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
