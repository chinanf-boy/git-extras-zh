
## Your new git-extra command should support

-   OSX,Linux,BSD(您可能需要浏览他们的手册页)<sup>\*</sup>
-   Bash 3.2+(如果你不确定,请参阅[the Bash changelog](http://tldp.org/LDP/abs/html/bash2.html))
-   Git 2.1+

<sup>\*</sup>如果您无法在平台上测试新命令,请在PR中清除该命令,其他人也可以在其系统上对其进行测试.

## To submit a new command, you should

我们假设您的新命令已命名`foo`.

1.  写下一个bash脚本`./bin`叫`git-foo`.
2.  读`./man/Readme.md`并编写文档`git-foo`.
3.  别忘了介绍它`Commands.md`.
4.  更新`./etc/git-extras-completion.zsh`.只需按照现有代码.
5.  (可选)更新`./etc/bash_completion.sh`.
6.  跑`./check_integrity.sh foo`检查是否全部完成.

欢迎您在打开拉取请求之前打开一个问题来讨论新的命令或功能.
