
# 安装 git-extras

## 用包管理器安装

### Debian

```bash
$ sudo $apt_pref update
$ sudo $apt_pref install git-extras
```

### Fedora

```bash
$ sudo dnf install git-extras
```

### RHEL/CentOS (要求 [EPEL](https://fedoraproject.org/wiki/EPEL))

```bash
$ sudo yum install git-extras
```

### Ubuntu

```bash
$ sudo apt-get install git-extras
```

### Nix/NixOS

```bash
$ nix-env -i git-extras
```

### Mac OS X with Homebrew

```bash
$ brew install git-extras
```

从brew安装不会给你省略`git-extras`某些选项，如果它们与现有的Git别名冲突. 要捯饬选项,请从源代码构建.

### Arch Linux

-   [git-extras](https://aur.archlinux.org/packages/git-extras/)
-   [git-extras-git](https://aur.archlinux.org/packages/git-extras-git/)

### Windows

- 首先,请安装`Git for Windows 2.x`从'[https://githubcom/git-fiondows/git/releases](https://github.com/git-for-windows/git/releases').

- 第二,克隆`git-extras`回购到任何你喜欢的文件夹.

```bash
git clone https://github.com/tj/git-extras.git
# checkout the latest tag (optional)
git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
```

之后,在命令提示符shell cmd下执行`install.cmd`.如果将Git安装为管理员,则需要将此提示符运行为管理员.默认情况下，它找到了`Git for Windows 2.x`如果它在路径中(在`where git.exe`wins的第一路径)或安装在默认位置`%ProgramFiles%\Git`. 后退是`C:\SCM\PortableGit`. 如果没有将Git安装到其中一个目录中，则必须为安装位置提供路径,例如如果安装在`c:\git`:

```batch
install.cmd "C:\git"
```

最后,若要使用`git line-summary`,`git summary`和`git ignore-io`，你需要从[msys2][1]上复制安装`folder-your-msys2-installed/usr/bin`的`column.exe`到`folder-your-git-installed/usr/bin`或者等待 Git 2.7.1,这版本将包括column.exe.

### BSD

使用下面的源代码构建.确保你正在使用`gmake`(GNU)`make`)而不是`make`.

## 从源码构建

通过克隆获得git-extras源[它的github repo](https://github.com/tj/git-extras.git)或者下载一个[版本](https://github.com/tj/git-extras/releases). 然后通过从源目录执行`make install`安装.

```bash
$ git clone https://github.com/tj/git-extras.git
$ cd git-extras
# checkout the latest tag
$ git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
$ [sudo] make install
```

默认情况下,git-extras安装在`/usr/local`. 若要将其安装在备用位置,请在执行`make`时指定`PREFIX`.

```bash
# 非管理员的用户可安装在自身目录
make install PREFIX=$HOME/software

# 第三方软件保存在 /opt
make install PREFIX=/opt
```

如果您想为已安装的大部分重新定位,但仍有配置文件安装到系统中`/etc`目录或其他替代位置,您可以添加指定`SYSCONFDIR`和`PREFIX`.

```
$ sudo make install PREFIX=/usr/local SYSCONFDIR=/etc
```

有关高级配置选项的详细信息,请参见Makefile.

## 网络安装

一行过:

```bash
curl -sSL http://git.io/git-extras-setup | sudo bash /dev/stdin
```

## 安装 作为 Zsh 插件

[Zplugin](https://github.com/zdharma/zplugin)可以安装git-extras，并使用:

```zsh
zplugin ice as"program" pick"$ZPFX/bin/git-*" make"PREFIX=$ZPFX"
zplugin light tj/git-extras
```

默认情况下`$ZPFX`是`~/.zplugin/polaris`.使用`zplugin update tj/git-extras`更新. 此方法安装在`$HOME`因此,您不需要管理员权限安装包.

## 更新

如果您使用包管理器安装了git-extras,请使用包管理器的工具来更新它.

如果从源码构建安装了git-extras部分,则可以运行`git-extras update`将其更新到最新版本.**请注意**,这可能会丢失在原始安装期间指定的任何配置选项.

享受`git-extras`!

[1]: http://sourceforge.net/projects/msys2/
