
-   [`git alias`](#git-alias)
-   [`git archive-file`](#git-archive-file)
-   [`git authors`](#git-authors)
-   [`git back`](#git-back)
-   [`git bug`](#git-featurerefactorbugchore)
-   [`git bulk`](#git-bulk)
-   [`git changelog`](#git-changelog)
-   [`git chore`](#git-featurerefactorbugchore)
-   [`git clear`](#git-clear)
-   [`git clear-soft`](#git-clear-soft)
-   [`git commits-since`](#git-commits-since)
-   [`git contrib`](#git-contrib)
-   [`git count`](#git-count)
-   [`git create-branch`](#git-create-branch)
-   [`git delete-branch`](#git-delete-branch)
-   [`git delete-merged-branches`](#git-delete-merged-branches)
-   [`git delete-submodule`](#git-delete-submodule)
-   [`git delete-tag`](#git-delete-tag)
-   [`git delta`](#git-delta)
-   [`git effort`](#git-effort)
-   [`git extras`](#git-extras)
-   [`git feature`](#git-featurerefactorbugchore)
-   [`git force-clone`](#git-force-clone)
-   [`git fork`](#git-fork)
-   [`git fresh-branch`](#git-fresh-branch)
-   [`git gh-pages`](#git-gh-pages)
-   [`git graft`](#git-graft)
-   [`git guilt`](#git-guilt)
-   [`git ignore`](#git-ignore)
-   [`git ignore-io`](#git-ignore-io)
-   [`git info`](#git-info)
-   [`git line-summary`](#git-line-summary)
-   [`git local-commits`](#git-local-commits)
-   [`git lock`](#git-lock)
-   [`git locked`](#git-locked)
-   [`git merge-into`](#git-merge-into)
-   [`git merge-repo`](#git-merge-repo)
-   [`git missing`](#git-missing)
-   [`git mr`](#git-mr)
-   [`git obliterate`](#git-obliterate)
-   [`git pr`](#git-pr)
-   [`git psykorebase`](#git-psykorebase)
-   [`git pull-request`](#git-pull-request)
-   [`git reauthor`](#git-reauthor)
-   [`git rebase-patch`](#git-rebase-patch)
-   [`git refactor`](#git-featurerefactorbugchore)
-   [`git release`](#git-release)
-   [`git rename-branch`](#git-rename-branch)
-   [`git rename-tag`](#git-rename-tag)
-   [`git repl`](#git-repl)
-   [`git reset-file`](#git-reset-file)
-   [`git root`](#git-root)
-   [`git rscp`](#git-scp)
-   [`git scp`](#git-scp)
-   [`git sed`](#git-sed)
-   [`git setup`](#git-setup)
-   [`git show-merged-branches`](#git-show-merged-branches)
-   [`git show-tree`](#git-show-tree)
-   [`git show-unmerged-branches`](#git-show-unmerged-branches)
-   [`git stamp`](#git-stamp)
-   [`git squash`](#git-squash)
-   [`git standup`](#git-standup)
-   [`git summary`](#git-summary)
-   [`git sync`](#git-sync)
-   [`git touch`](#git-touch)
-   [`git undo`](#git-undo)
-   [`git unlock`](#git-unlock)

## git extras

主要的`git-extras`命令.

输出电流`--version`:

```bash
$ git extras
```

列出可用命令:

```bash
$ git extras --help
```

更新到最新版本`git-extras`:

```bash
$ git extras update
```

## git gh-pages

设置`gh-pages`科.(看到[GitHub Pages](http://pages.github.com/)文档).

## git feature|refactor|bug|chore

创建/合并给定的功能,重构,错误或杂项分支`name`:

```bash
$ git feature dependencies
```

要设置远程跟踪分支:

```bash
$ git feature dependencies -r upstream
```

*注意*:如果没有传递远程名称`-r`选项,它将推动*起源*.

之后,相同的命令将检查出来:

```bash
$ git checkout master
$ git feature dependencies
```

完成后,我们可以`feature finish`将其合并到当前分支:

```bash
$ git checkout master
$ git feature finish dependencies
```

*注意*:如果设置了一个遥控器来跟踪分支,它将被删除.

所有这一切都有效`feature`,`bug`,`chore`要么`refactor`.

## git contrib

产量`author`对项目的贡献:

```bash
$ git contrib visionmedia
visionmedia (18):
  Export STATUS_CODES
  Replaced several Array.prototype.slice.call() calls with Array.prototype.unshift.call()
  Moved help msg to node-repl
  Added multiple arg support for sys.puts(), print(), etc.
  Fix stack output on socket error
  ...
```

## git summary

输出回购摘要:

```bash
$ git summary

project  : git-extras
repo age : 10 months ago
commits  : 163
active   : 60 days
files    : 93
authors  :
   97   Tj Holowaychuk          59.5%
   37   Jonhnny Weslley         22.7%
    8   Kenneth Reitz           4.9%
    5   Aggelos Orfanakos       3.1%
    3   Jonathan "Duke" Leto    1.8%
    2   Gert Van Gool           1.2%
    2   Domenico Rotiroti       1.2%
    2   Devin Withers           1.2%
    2   TJ Holowaychuk          1.2%
    1   Nick Campbell           0.6%
    1   Alex McHale             0.6%
    1   Jason Young             0.6%
    1   Jens K. Mueller         0.6%
    1   Guillermo Rauch         0.6%
```

这个命令也可以带一个*commitish*,并将在提交范围内打印提交摘要:

```bash
$ git summary v42..
```

此命令也可以选择`--line`,将按行打印摘要

```bash
$ git summary --line

project  : git-extras
 lines    : 8420
 authors  :
 2905 Tj Holowaychuk            34.5%
 1901 Jonhnny Weslley           22.6%
 1474 nickl-                    17.5%
  653 Leila Muhtasib            7.8%
  275 Tony                      3.3%
  267 Jesús Espino             3.2%
  199 Philipp Klose             2.4%
  180 Michael Komitee           2.1%
  178 Tom Vincent               2.1%
  119 TJ Holowaychuk            1.4%
  114 Damian Krzeminski         1.4%
   66 Kenneth Reitz             0.8%
   22 Not Committed Yet         0.3%
   17 David Baumgold            0.2%
   12 Brian J Brennan           0.1%
    6 Leandro López            0.1%
    6 Jan Krueger               0.1%
    6 Gunnlaugur Thor Briem     0.1%
    3 Hogan Long                0.0%
    3 Curtis McEnroe            0.0%
    3 Alex McHale               0.0%
    3 Aggelos Orfanakos         0.0%
    2 Phally                    0.0%
    2 NANRI                     0.0%
    2 Moritz Grauel             0.0%
    1 Jean Jordaan              0.0%
    1 Daniel Schildt            0.0%
```

## git line-summary

警告:git line-summary已被替换为[`git summary --line`](#git-summary)并将在以后的版本中删除.

## git effort

显示"工作量"统计信息,当前只是每个文件的提交数量,显示突出显示活动最多的位置."活动天数"列是对此文件进行修改的总天数.

```
node (master): git effort --above 15 {src,lib}/*
```

  ![git effort](http://f.cl.ly/items/0b0w0S2K1d100e2T1a0D/Screen%20Shot%202012-02-08%20at%206.43.34%20PM.png)

如果您希望忽略带有提交的文件`<=`您可以使用的价值`--above`:

```
$ git effort --above 5
```

如果您希望仅查看上个月的提交,则可以使用`--since`(它支持相同的语法,如`git log --since`):

```
 $ git effort -- --since='last month'
```

默认情况下`git ls-files`使用,但您可以传递一个或多个文件`git-effort(1)`, 例如:

```
$ git effort bin/* lib/*
```

## git bulk

`git bulk`为您希望在多个git存储库上执行的操作添加方便的支持.

-   只需在其目录结构中注册包含多个git repos的工作区
-   在一个命令中对已注册工作区的存储库运行任何git命令`git bulk`
-   使用"保护模式"检查每次执行

```bash
usage: git bulk [-g] ([-a]|[-w <ws-name>]) <git command>
       git bulk --addworkspace <ws-name> <ws-root-directory>
       git bulk --removeworkspace <ws-name>
       git bulk --addcurrent <ws-name>
       git bulk --purge
       git bulk --listall
```

注册工作区以便这样做`git bulk`了解它(请注意<ws-root-directory>必须是绝对路径):

```bash
$ git bulk --addworkspace personal ~/workspaces/personal
```

将当前目录注册为工作空间`git bulk`

```bash
$ git bulk --addcurrent personal
```

列出所有已注册的工作区:

```bash
$ git bulk --listall
bulkworkspaces.personal /Users/niklasschlimm/workspaces/personal
```

在当前工作空间的存储库上运行git命令:

```bash
$ git bulk fetch
```

![fetchdemo](https://cloud.githubusercontent.com/assets/876604/23709805/e8178406-041a-11e7-9a0c-01de5fbf8944.png)

在一个特定工作区及其存储库上运行git命令:

```bash
$ git bulk -w personal fetch
```

在所有工作区及其存储库上运行git命令:

```bash
$ git bulk -a fetch
```

运行git命令,但要求用户确认每次执行(保护模式):

```bash
$ git bulk -g fetch
```

删除已注册的工作区:

```bash
$ git bulk --removeworkspace personal
```

删除所有已注册的工作区:

```bash
$ git bulk --purge
```

## git repl

Git read-eval-print-loop.我们跑吧`git`没有输入'git'的命令.

命令可以带有感叹号(!)作为前缀,以解释为常规命令.

类型`exit`要么`quit`结束repl会话.

```bash
$ git repl
git version 2.9.2
git-extras version 3.0.0
type 'ls' to ls files below current directory,
'!command' to execute any command or just 'subcommand' to execute any git subcommand

git (master)> ls-files
History.md
Makefile
Readme.md
bin/git-changelog
bin/git-count
bin/git-delete-branch
bin/git-delete-tag
bin/git-ignore
bin/git-release

git (master)> !echo Straight from the shell!
Straight from the shell!

git (master)> quit
```

## git commits-since

列表提交以来`date`(默认为"上周"):

```bash
$ git commits-since
... changes since last week
TJ Holowaychuk - Fixed readme
TJ Holowaychuk - Added git-repl
TJ Holowaychuk - Added git-delete-tag
TJ Holowaychuk - Added git-delete-branch

$ git commits-since yesterday
... changes since yesterday
TJ Holowaychuk - Fixed readme
```

## git count

输出提交计数:

```bash
$ git count

total 1844
```

输出详细提交计数:

```bash
$ git count --all

visionmedia (1285)
Tj Holowaychuk (430)
Aaron Heckmann (48)
csausdev (34)
ciaranj (26)
Guillermo Rauch (6)
Brian McKinney (2)
Nick Poulden (2)
Benny Wong (2)
Justin Lilly (1)
isaacs (1)
Adam Sanderson (1)
Viktor Kelemen (1)
Gregory Ritter (1)
Greg Ritter (1)
ewoudj (1)
James Herdman (1)
Matt Colyer (1)

total 1844
```

## git fork

分叉给定的github\<回购>.像克隆,但首先分叉.

```Shell
$ git fork https://github.com/LearnBoost/expect.js
```

要不就:

```Shell
$ git fork LearnBoost/expect.js
```

以下是:

-   for the repo(提示输入github用户名并通过)
-   将repo克隆到当前目录中
-   将原始仓库添加为远程仓库,以便跟踪上游变更
-   如果配置了所有遥控器refs在ssh上使用git,否则将使用https

```Shell
$ cd expect.js && git remote -v
origin          git@github.com:<user>/expect.js (fetch)
origin          git@github.com:<user>/expect.js (push)
upstream        git@github.com:LearnBoost/expect.js (fetch)
upstream        git@github.com:LearnBoost/expect.js (push)
```

## git force-clone

如果克隆目标目录存在并且是git存储库,请将其内容重置为远程克隆.

```bash
$ git force-clone [-b {branch_name}] {remote_url} {destination_path}
$ git force-clone -b master https://github.com/tj/git-extras ./target-directory
```

**警告**:如果存储库存在,则会破坏*所有*对存储库的本地更改 - 将更改已更改的文件,并将删除本地分支.

[More information](man/git-force-clone.md).

## git release

使用给定的释放提交\<标签>和其他选择:

```bash
$ git release 0.1.0
```

如果你正在使用[semver](https://semver.org)在您的项目中,您还可以使用以下命令:(运行`git help release`欲获得更多信息)

```bash
$ git release --semver major/minor/patch
```

以下是:

-   执行*的.git /钩/ pre-release.sh*(如果存在),传递给定标记并保留参数
-   通过消息"发布"提交更改(更改日志等)\<标签>"
-   标签与给定\<标签>
-   推动分支/标签
-   执行*的.git /钩/ post-release.sh*(如果存在),传递给定标记并保留参数

## git rename-branch

在本地重命名分支,并通过同步到远程`git push`.

```
# renames any branch
$ git rename-branch new-name old-name

# renames current branch
$ git rename-branch new-name
```

## git rename-tag

重命名标记(本地和远程).

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

## git reauthor

重写历史记录以更改作者的身份.

将个人电子邮件和杰克的名字替换为他的工作

```bash
$ git reauthor --old-email jack@perso.me --correct-email jack@work.com --correct-name 'Jack Foobar'
```

将Jack的电子邮件和名称替换为Git配置中定义的名称

```bash
$ git reauthor --old-email jack@perso.me --use-config
```

仅替换Jack的电子邮件(保留已使用的名称)

```bash
$ git reauthor --old-email jack@perso --correct-email jack@perso.me
```

仅更改Jack的提交者电子邮件(保留已使用的作者电子邮件)

```bash
$ git reauthor --old-email jack@perso.me --correct-email jack@work.com --type committer
```

将Jack的身份设置为整个存储库中唯一的一个

```bash
$ git reauthor --all --correct-email jack@perso.me --correct-name Jack
```

将Jack设置为整个存储库的唯一提交者(保留作者)

```bash
$ git reauthor --all --correct-email jack@perso.me --correct-name Jack --type committer
```

## git alias

定义,搜索和显示别名.

定义一个新别名:

```bash
$ git alias last "cat-file commit HEAD"
```

搜索与模式匹配的别名(一个参数):

```bash
$ git alias ^la
last = cat-file commit HEAD
```

显示所有别名(无参数):

```bash
$ git alias
s = status
amend = commit --amend
rank = shortlog -sn --no-merges
whatis = show -s --pretty='tformat:%h (%s, %ad)' --date=short
whois = !sh -c 'git log -i -1 --pretty="format:%an <%ae>
```

## git ignore

懒得开口`.gitignore`?我也是!

```bash
$ git ignore build "*.o" "*.log"
... added 'build'
... added '*.o'
... added '*.log'
```

没有任何图案,`git-ignore`显示当前在全局和本地中忽略的模式`.gitignore`文件:

```bash
$ git ignore
Global gitignore: /Users/foo/.gitignore_global
*~
.metadata
---------------------------------
Local gitignore: .gitignore
build
*.o
*.log
```

要仅显示全局文件或本地文件的内容,可以使用以下可选参数:

-   `-g`要么`--global`仅显示全局文件
-   `-l`要么`--local`只显示本地文件
-   `-p`要么`--private`只显示存储库的文件

```bash
$ git ignore -g
Global gitignore: /Users/foo/.gitignore_global
*~
.metadata
```

```bash
$ git ignore -l
Local gitignore: .gitignore
build
*.o
*.log
```

## git ignore-io

从中生成样本gitignore文件[gitignore.io](https://www.gitignore.io)

没有选项,`git ignore-io <type>`在屏幕上显示指定类型的示例gitignore.

```bash
$ git ignore-io vim

    # Created by https://www.gitignore.io/api/vim

    ### Vim ###
    [._]*.s[a-w][a-z]
    [._]s[a-w][a-z]
    *.un~
    Session.vim
    .netrwhist
    *~
```

将其导出到`.gitignore`文件您可以使用以下选项:

-   `-a`要么`--append`将结果追加到`.gitignore`
-   `-r`要么`--replace`出口`.gitignore`结果

```bash
$ git ignore-io vim python
```

为了提高效率`git ignore-io`存储所有可用的类型`~/.gi_list`.列出所有可用类型:

-   `-l`要么`-L`:这两个选项将以不同的格式显示列表.就试一试吧.

您还可以通过以下方式从列表中搜索类型:

-   `-s <word>`要么`--search <word>`

```bash
$ git ignore-io -s ja

    django
    jabref
    java
    ninja
```

## git info

显示有关回购的信息:

```bash
$ git info

    ## Remote URLs:

    origin              git@github.com:sampleAuthor/git-extras.git (fetch)
    origin              git@github.com:sampleAuthor/git-extras.git (push)

    ## Remote Branches:

    origin/HEAD -> origin/master
    origin/myBranch

    ## Local Branches:

    myBranch
    * master

    ## Most Recent Commit:

    commit e3952df2c172c6f3eb533d8d0b1a6c77250769a7
    Author: Sample Author <sampleAuthor@gmail.com>

    Added git-info command.

    Type 'git log' for more commits, or 'git show <commit id>' for full commit details.

    ## Configuration (.git/config):

    color.diff=auto
    color.status=auto
    color.branch=auto
    user.name=Sample Author
    user.email=sampleAuthor@gmail.com
    core.repositoryformatversion=0
    core.filemode=true
    core.bare=false
    core.logallrefupdates=true
    core.ignorecase=true
    remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
    remote.origin.url=git@github.com:mub/git-extras.git
    branch.master.remote=origin
    branch.master.merge=refs/heads/master
```

如果您想省略配置部分,您可以使用`--no-config`:

```bash
$ git info --no-config
```

## git create-branch

创建本地分支`name`:

```bash
$ git create-branch development
```

创建本地分支`name`并设置远程跟踪分支`origin`:

```bash
$ git create-branch -r development
```

创建本地分支`name`并设置远程跟踪分支`upstream`:

```bash
$ git create-branch -r upstream development
```

## git delete-branch

删除本地和远程分支`name`:

```bash
$ git delete-branch integration
```

## git delete-submodule

删除子模块`name`:

```bash
$ git delete-submodule lib/foo
```

## git delete-tag

删除本地和远程标记`name`:

```bash
$ git delete-tag 0.0.1
```

## git delete-merged-branches

删除列出的分支`git branch --merged`.

```bash
$ git delete-merged-branches
Deleted feature/themes (was c029ab3).
Deleted feature/live_preview (was a81b002).
Deleted feature/dashboard (was 923befa).
...
```

## git fresh-branch

创建空的本地分支`name`:

```bash
$ git fresh-branch docs
```

## git guilt

计算两次修订之间的责任变化

```bash
# Find blame delta over the last three weeks
$ git guilt `git log --until="3 weeks ago" --format="%H" -n 1` HEAD
Paul Schreiber                +++++++++++++++++++++++++++++++++++++++++++++(349)
spacewander                   +++++++++++++++++++++++++++++++++++++++++++++(113)
Mark Eissler                  ++++++++++++++++++++++++++
CJ                            +++++
nickl-                        -
Jesse Sipprell                -
Evan Grim                     -
Ben Parnell                   -
hemanth.hm                    --
```

## git merge-into

合并`src`分支`dest`,并保持自己的当前分支.如果`src`分支没有给出,它将合并当前的一个`dest`:

```bash
$ git merge-into [src] dest
```

## git graft

合并提交`src-branch`成`dest-branch`.

```bash
$ git graft new_feature master
```

## git squash

合并提交`src-branch`进入当前分支机构*单*承诺.如果提供了当前分支的提交引用,也可以使用.什么时候`[msg]`给出`git-commit(1)`将使用该消息调用.当主题分支中的小型单个提交无关紧要并且您希望将主题视为单个更改时,这非常有用.

```bash
$ git squash fixed-cursor-styling
$ git squash fixed-cursor-styling "Fixed cursor styling"
$ git squash 95b7c52
$ git squash HEAD~3
$ git squash HEAD~3 "Work on a feature"
```

## git authors

填充文件匹配`authors|contributors -i`根据每位作者的提交数量,与提交的作者一起.

打开文件`$EDITOR`什么时候设定

见["MAPPING AUTHORS" section](http://git-scm.com/docs/git-shortlog#_mapping_authors)的**混帐shortlog**(1)由同一人合并提交.

更新AUTHORS文件:

```bash
$ git authors && cat AUTHORS

TJ Holowaychuk <tj@vision-media.ca>
hemanth.hm <hemanth.hm@gmail.com>
Jonhnny Weslley <jw@jonhnnyweslley.net>
nickl- <github@jigsoft.co.za>
Leila Muhtasib <muhtasib@gmail.com>
```

上市作者:

```bash
$ git authors --list

TJ Holowaychuk <tj@vision-media.ca>
hemanth.hm <hemanth.hm@gmail.com>
Jonhnny Weslley <jw@jonhnnyweslley.net>
nickl- <github@jigsoft.co.za>
Leila Muhtasib <muhtasib@gmail.com>
```

上传作者没有电子邮件

```bash
$ git authors --list --no-email

TJ Holowaychuk
hemanth.hm
Jonhnny Weslley
nickl-
Leila Muhtasib
```

## git back

删除最新提交,并将其更改添加到临时区域.

```
$ git back # Removes the latest commit.
$ git back 3 # Remove the latest 3 commits.
```

## git changelog

从git(1)标记(带注释或轻量级)生成更改日志并提交消息.文件名以.开头的现有changelog文件*更改*要么*历史*将使用不区分大小写的匹配模式自动识别,并且现有内容将附加到生成的新输出 - 可以通过指定剪枝选项(-p | --prune-old)来禁用此行为.生成的文件将在中打开**$ EDITOR**什么时候设定

如果不存在标签,则输出所有提交;如果标签存在,那么只有最近的提交输出到最后识别的标签.可以通过指定一个或两个范围选项(-f | --final-tag和-s | --start-tag)来更改此行为.

可以使用以下选项:

```bash
  -a, --all                 Retrieve all commits (ignores --start-tag, --final-tag)
  -l, --list                Display commits as a list, with no titles
  -t, --tag                 Tag label to use for most-recent (untagged) commits
  -f, --final-tag           Newest tag to retrieve commits from in a range
  -s, --start-tag           Oldest tag to retrieve commits from in a range
  -n, --no-merges           Suppress commits from merged branches
  -p, --prune-old           Replace existing Changelog entirely with new content
  -x, --stdout              Write output to stdout instead of to a Changelog file
  -h, --help, ?             Usage help
```

类型`git changelog --help`用于基本用途或`man git-changelog`欲获得更多信息.

**注意:**默认情况下,`git changelog`将任何检测到的更改日志的内容连接到其输出.使用`-p`用于防止此行为的选项.

### Examples

生成一个新的更改日志,其中包含自上一个标记以来的所有提交,使用标记名称*1.5.2*对于此最近提交部分的标题(日期将自动生成为今天的日期):

```bash
$ git changelog --tag 1.5.2 && cat History.md

1.5.2 / 2015-03-15
==================

* Docs for git-ignore. Closes #3
* Merge branch 'ignore'
* Added git-ignore
* Fixed <tag> in docs
* Install docs
* Merge branch 'release'
* Added git-release
* Passing args to git shortlog
* Added --all support to git-count
```

列出自上一个标记以来的所有提交:

```bash
$ git changelog --list

* Docs for git-ignore. Closes #3
* Merge branch 'ignore'
* Added git-ignore
* Fixed <tag> in docs
* Install docs
* Merge branch 'release'
* Added git-release
* Passing args to git shortlog
* Added --all support to git-count
```

列出从一开始就提交的所有提交:

```bash
$ git changelog --list --all

* Docs for git-ignore. Closes #3
* Merge branch 'ignore'
* Added git-ignore
* Fixed <tag> in docs
* Install docs
* Merge branch 'release'
* Added git-release
* Passing args to git shortlog
* Added --all support to git-count
...
<many many commits>
...
* Install docs.
* Merge branch 'release'.
* Added 'git-release'.
* Fixed readme.
* Passing args to git shortlog.
* Initial commit
```

## git undo

删除最新提交:

```bash
git undo
```

删除最新的3次提交:

```bash
git undo 3
```

## git sed

按照指示运行grep,但用模式替换给定的文件.

## git setup

设置一个git存储库(如果不存在),添加所有文件,并进行初始提交.`dir`默认为当前工作目录.

## git scp

将文件从当前工作树复制到远程存储库的工作目录的便捷方法.如果一个`<commits>...`如果提供,则仅复制在提交范围内已更改的文件.

这个脚本在内部使用`rsync`并不是`scp`顾名思义.

`git-rscp`- 相反的`git-scp`.将特定文件从远程存储库的工作目录复制到当前工作目录.

### Examples

将未分段的文件复制到远程.当您想要在不进行任何提交的情况下进行快速测试时非常有用

```
$ git scp staging
```

将暂存和未暂存的文件复制到远程

```
$ git scp staging HEAD
```

将上次提交中已更改的文件以及任何已暂存或未暂存的文件复制到远程

```
$ git scp staging HEAD~1
```

复制现在和标签之间已更改的文件

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

## git show-merged-branches

显示合并到当前HEAD的所有分支.

## git show-unmerged-branches

显示所有分支**不**合并到当前的HEAD.

## git show-tree

显示所有分支的一个衬垫汇总提交的装饰图形视图.例如,跑步`git show-tree`将显示:

```
*   4b57684 (HEAD, develop) Merge branch upstream master.
|\
| *   515e94a Merge pull request #128 from nickl-/git-extras-html-hyperlinks
| |\
| | * 815db8b (nickl/git-extras-html-hyperlinks, git-extras-html-hyperlinks) help ronn make hyperlinks.
| * | 7398d10 (nickl/develop) Fix #127 git-ignore won't add duplicates.
| |/
| | * ab72c1e (refs/stash) WIP on develop: 5e943f5 Fix #127 git-ignore won't add duplicates.
| |/
|/|
* | 730ca89 (bolshakov) Rebase bolshakov with master
|/
* 60f8371 (origin/master, origin/HEAD, master) Merge pull request #126 from agrimaldi/fix-changelog-last-tag
...
```

可以自由尝试!

## git stamp

标记最后一次提交消息

提交消息是

```bash
Fix timezone bug
```

从您的错误跟踪器中引用问题编号

```bash
$ git stamp Issue FOO-123

commit 787590e42c9bacd249f3b79faee7aecdc9de28ec
Author: Jack <jack@work.com>
Commit: Jack <jack@work.com>

    Fix timezone bug

    Issue FOO-123

$ git stamp Issue FOO-456 \#close

commit f8d920511e052bea39ce2088d1d723b475aeff87
Author: Jack <jack@work.com>
Commit: Jack <jack@work.com>

    Fix timezone bug

    Issue FOO-123

    Issue FOO-456 #close
```

链接到其评论页面

```bash
$ git stamp Review https://reviews.foo.org/r/4567/

commit 6c6bcf43bd32a76e37b6fc9708d3ff0ae723c7da
Author: Jack <jack@work.com>
Commit: Jack <jack@work.com>

    Fix timezone bug

    Issue FOO-123

    Issue FOO-456 #close

    Review https://reviews.foo.org/r/4567/
```

用新的问题替换以前的问题(注意标识符不区分大小写)

```bash
$ git stamp --replace issue BAR-123

commit 2b93c56b2340578cc3478008e2cadb05a7bcccfa
Author: Jack <jack@work.com>
Commit: Jack <jack@work.com>

    Fix timezone bug

    Review https://reviews.foo.org/r/4567/

    issue BAR-123
```

## git standup

回想一下你做了什么,或者在给定的时间范围内找到别人做了什么.例如,回忆一下自上周(7天前)John的提交:

```
git standup -a John -d 7
```

## git touch

呼叫`touch`在给定文件上,并将其添加到当前索引.一步创建新文件.

## git obliterate

从存储库中完全删除文件,包括过去的提交和标记.

```bash
git obliterate secrets.json
```

## git local-commits

列出本地分支上尚未发送到源的所有提交.任何其他参数将直接传递给git log.

## git archive-file

创建当前git存储库的zip存档.归档的名称将取决于您的git存储库的当前HEAD.

## git missing

打印出哪些提交在一个分支或另一个分支上,但不是两个.

```bash
$ git missing master
< d14b8f0 only on current checked out branch
> 97ef387 only on master
```

## git lock

锁定本地文件`filename`:

```bash
$ git lock config/database.yml
```

## git locked

列出本地锁定文件:

```bash
$ git locked
config/database.yml
```

## git unlock

解锁本地文件`filename`

```bash
$ git unlock config/database.yml
```

## git reset-file

将一个文件重置为`HEAD`或某些提交

将一个文件重置为HEAD

```bash
$ git reset-file .htaccess
```

或将一个文件重置为某个提交

```bash
$ git reset-file .htaccess dc82b19
```

## git mr

检查来自GitLab的合并请求.用法:`git mr <ID|URL> [REMOTE]`.默认远程是`origin`.

```bash
$ git mr 51
From gitlab.com:owner/repository
 * [new ref]         refs/merge-requests/51/head -> mr/51
Switched to branch 'mr/51'
```

使用完整URL,将从指向基本URL的临时远程提取头部.

```bash
$ git mr https://gitlab.com/owner/repository/merge_requests/51 
From gitlab.com:owner/repository
 * [new ref]         refs/merge-requests/51/head -> mr/51
Switched to branch 'mr/51'
```

就像[git pr](#git-pr),`git mr`接受一个`clean`废弃所有人的论点`mr/`分支机构.确保当前分支不是一个.

## git pr

查看来自GitHub的拉取请求

```bash
$ git pr 226
From https://github.com/tj/git-extras
 * [new ref]       refs/pulls/226/head -> pr/226
Switched to branch 'pr/226'
```

使用除以外的遥控器`origin`,例如`upstream`如果您正在使用fork,请将其指定为第二个参数:

```bash
$ git pr 226 upstream
From https://github.com/tj/git-extras
 * [new ref]       refs/pulls/226/head -> pr/226
Switched to branch 'pr/226'
```

您还可以根据GitHub网址查看拉取请求

```bash
$ git pr https://github.com/tj/git-extras/pull/453
From https://github.com/tj/git-extras
 * [new ref]         refs/pull/453/head -> pr/453
Switched to branch 'pr/453'
```

要删除所有本地拉取请求分支,请提供魔术`clean`参数:

```bash
$ git pr clean
Deleted branch 'pr/226' (was 1234567).
```

## git root

显示git repo根目录的路径

```bash
$ pwd
.../very-deep-from-root-directory
$ cd `git root`
$ git add . && git commit
```

## git delta

列出与其他分支不同的文件.

```bash
$ touch README.md
$ git setup
$ git checkout -b hello
$ echo hello >> README.md
$ git delta
README.md
$ touch Makefile
$ git add Makefile
$ git delta
Makefile
README.md
```

## git clear

是否进行硬重置并从工作目录中删除所有未跟踪的文件,包括.gitignore中的文件.

## git clear-soft

是否重置并删除工作目录中所有未跟踪的文件,不包括.gitignore中的文件.

## git merge-repo

合并两个存储库历史记录.

```bash
$ git merge-repo other-repo.git master new_dir
```

以上合并`other-repo.git`的`master`分支到当前存储库中`new_dir`目录.

```bash
$ git merge-repo git@github.com:tj/git-extras.git master .
```

上面合并了一个远程仓库`master`分支到当前存储库的目录,而不是保留历史记录.

## git psykorebase

使用合并提交和仅一个冲突处理将分支重新基于另一个分支.

```bash
$ git psykorebase master
```

以上重新定位当前分支`master`分公司.

```bash
$ git psykorebase --continue
```

冲突处理后,上述情况继续发生变化.

```bash
$ git psykorebase master feature
```

以上的变种`feature`分支在上面`master`科

## git pull-request

通过命令行创建拉取请求.

## git rebase-patch

鉴于您有一个不适用于当前HEAD的补丁,但您知道它过去适用于某些提交,`git rebase-patch`将帮助您找到提交并进行rebase.

例如,

```
$ git rebase-patch test.patch
Trying to find a commit the patch applies to...
Patch applied to dbcf408dd26 as 7dc8b23ae1a
First, rewinding head to replay your work on top of it...
Applying: test.patch
Using index info to reconstruct a base tree...
Falling back to patching base and 3-way merge...
Auto-merging README.txt
```

然后你的最后一次提交有补丁的更改并命名`test.patch`.

## git sync

将本地分支与其远程分支同步

```bash
$ git sync
```

将本地分支与origin / master同步

```bash
$ git sync origin master
```
