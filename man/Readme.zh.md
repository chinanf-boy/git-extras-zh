
# 如何:生成文档

## 描述

生成文档:

1) 开始`man-template.md`的填写

2) 然后安装ronn程序.[ronn 的 github.](https://github.com/rtomayko/ronn)

3) 运行

```
$ make -C .. man/git-<command>.{1,html}
```

4) 记住,我们使用下面的文件命名规则为:

```
git-<command>.html
git-<command>.1
git-<command>.md
```

## 作者

- 书写 Leila Muhtasib\<<mailto:muhtasib@gmail.com>>

- 脚本 Nick Lombard\<<mailto:github@jigsoft.co.za>>

## 漏洞报告

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
