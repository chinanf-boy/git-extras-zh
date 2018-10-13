
# Git批量(1)——在多个存储库上运行Git命令

## 简介

用法:用法:[-g]\([-a]γ[-w &lt;WS名称-])\<GIT命令>git块——AdWorkWorkStudio\<WS名称> \<WS根目录>Git批量-删除工作空间\<WS名称>Git批量-附加电流\<WS名称>Git批量-清除Git批量-列表

## 描述

Git批量为您希望在多个Git存储库上执行的操作提供方便的支持.

-   只需在目录结构中注册包含多个Git RePOS的工作区
-   在一个命令中在注册工作区的存储库上运行任何Git命令`git bulk`
-   使用"守卫模式"检查每个执行

## 选项

  \-a

在所有工作区及其存储库上运行Git命令.

  \-g

要求用户在每次执行时确认.

  \-w \<WS名称>

在指定的工作区上运行Git命令.必须注册工作区.

  \<GIT命令>

您希望在存储库上执行的任何Git命令.

\-- AdWorkStudio\<WS名称> \<WS根目录>

为大容量操作注册工作区.下面的所有存储库\<WS根目录>用名称在这个工作区注册\<WS名称>. \<WS根目录>必须是绝对路径.

\--删除工作区\<WS名称>

用逻辑名称删除工作区\<WS名称>.

\--附加电流\<WS名称>

将当前目录作为工作区添加到Git批量操作中.工作空间以其逻辑名引用.\<WS名称>.

清灰-吹扫

移除所有定义的存储库位置.

Git批量-列表

列出所有已注册的存储库.

## 实例

```
Register a workspace so that git bulk knows about it:

$ git bulk --addworkspace personal ~/workspaces/personal

Register the current directory as a workspace to git bulk:

$ git bulk --addcurrent personal

List all registered workspaces:

$ git bulk --listall

Run a git command on the repositories of the current workspace:

$ git bulk fetch

Run a git command on the specified workspace and its repositories:

$ git bulk -w personal fetch

Run a git command but ask the user for confirmation on every execution (guarded mode):

$ git bulk -g fetch

Remove a registered workspace:

$ git bulk --removeworkspace personal

Remove all registered workspaces:

$ git bulk --purge
```

## 作者

Niklas Schlimm笔下\<<mailto:ns103@hotmail.de>>

## 报告错误

\<[https://github.com/nschlimm/git-bulk>](https://github.com/nschlimm/git-bulk&gt);

## 也见

\<<https://github.com/tj/git-extras>>
