###安裝brew
**说明：**

Homebrew，是Mac OSX的软件包管理工具，安裝或者卸载软件非常方便，类似Linux下的apt-get

**安装方法：**

- 方法一：ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
- 方法二：curl -LsSf http://github.com/mxcl/homebrew/tarball/master | sudo tar xvz -C/usr/local --strip 1

**例子：**
sudo brew install wget
sudo brew uninstall wget 

--------------------------------------------
###安装oh my zsh
**说明：**

Linux/Unix提供了很多种shell，常用的shell有sh、bash、csh，执行命令cat /etc/shells可以系统有几种shell

```
/bin/bash
/bin/csh
/bin/ksh
/bin/sh
/bin/tcsh
/bin/zsh
```
zsh就是shell中的一种，但是配置复杂，于是有大神就开发了oh my zsh

**安装方法：**

- 方法一：sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
- 方法二：sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

**配置：**

1. 设置zsh为默认的shell  
```
chsh -s /bin/zsh
```
2. 使用主题（推荐使用agnoster）

- 下载agnoster主题

```
vi ~/.zshrc //打开配置文件
```