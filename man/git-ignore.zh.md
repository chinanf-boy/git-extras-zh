
# Git忽略(1)-Addio.GiTigGORE模式

## 简介

`git-ignore` [&lt;语境&gt;]\<模式> [&lt;模式&gt;]……

## 描述

如果已经存在,则将给定的yTopnnIs添加到.GiTigNoR文件.

## 选项

  \<语境>

\-L,局部

将上下文设置为当前工作目录中的.GiTigNoRE文件.(默认)

\-G,-全球

将上下文设置为当前用户的全局GiTigGORE文件.

\-P,-私人

为存储库的私有排除文件设置上下文(`.git/info/exclude`)

  \<模式>

在上下文中附加到文件的空间分隔的模式列表.

### 模式格式

Git手册中描述的模式格式

-   空白行不匹配文件,因此它可以作为可读性的分隔符.要追加空白行,请使用"空引号".

-   一个以"开始"开头的行作为注释.例如,"这是一个评论"

-   一个可选的前缀!它否定了该模式;由先前模式排除的任何匹配文件将再次被包含.如果否定模式匹配,则将重写较低优先级的模式源.用感叹词!作为命令行参数,它最好放置在单引号之间.例如,'!型钢混凝土

-   如果模式以斜线结尾,则出于以下描述的目的而将其删除,但是它只能找到与目录的匹配.换句话说,foo/将匹配目录foo及其下面的路径,但不匹配常规文件或符号链接foo(这与pathspec在git中一般工作方式是一致的).

-   如果模式不包含斜杠/,则git将其视为shell glob模式,并检查路径名与.gitignore文件的位置(如果不是来自.gitignore文件,则相对于工作树的顶层)的匹配.

-   否则,git将模式视为适合fnmatch(3)使用FNM_PATHNAME标志消费的shell glob:模式中的通配符将不匹配路径名中的a.例如,"Documentation/\*.html"匹配"Documentation/git.html",但不匹配"Documentation/ppc/ppc.html"或"tools/perf/Documentation/perf.html".

-   一个领先的斜杠匹配路径名的开头.例如,"/\*.c"匹配"CAT文件.c",而不是"MyZILA-SHI1/SHA1.C".

## 实例

所有参数都是可选的,所以只调用Git忽略将首先显示全局,然后显示本地GiTigGORE文件:

```
$ git ignore
Global gitignore: /home/alice/.gitignore
# Numerous always-ignore extensions
*.diff
*.err
*.orig
*.rej
*.swo
*.swp
*.vi
*~
*.sass-cache

# OS or Editor folders
.DS_Store
.Trashes
._*
Thumbs.db
---------------------------------
Local gitignore: .gitignore
.cache
.project
.settings
.tmproj
nbproject
```

如果只想查看全局上下文,请使用-Global参数(用于本地使用-本地):

```
$ git ignore
Global gitignore: /home/alice/.gitignore
.DS_Store
.Trashes
._*
Thumbs.db
```

简单地将新模式追加到默认/本地上下文:

```
$ git ignore *.log
Adding pattern(s) to: .gitignore
... adding '*.log'
```

现在,您无需使用编辑器,就可以使用上下文和模式参数配置任何模式:为了方便起见,还会返回结果配置.

```
$ git ignore --local "" "# Temporary files" *.tmp "*.log" tmp/*  "" "# Files I'd like to keep" '!work'  ""
Adding pattern(s) to: .gitignore
... adding ''
... adding '# Temporary files'
... adding 'index.tmp'
... adding '*.log'
... adding 'tmp/*'
... adding ''
... adding '# Files I'd like to keep'
... adding '!work'
... adding ''

Local gitignore: .gitignore

# Temporary files
index.tmp
*.log

# Files I'd like to keep
!work
```

## 作者

Tj Holowaychuk笔下\<<mailto:tj@vision-media.ca>>Tema Bolshakov\<<mailto:tweekane@gmail.com>>Nick Lombard\<<mailto:github@jigsoft.co.za>>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>
