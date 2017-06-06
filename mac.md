###安装iterm2
**说明：**

mac系统上替代终端的命令行工具

**安装方法：**

直接从官网下载安装即可，[下载地址](http://www.iterm2.com/)

-------------------------------
###安裝brew
**说明：**

Homebrew，是Mac OSX的软件包管理工具，安裝或者卸载软件非常方便，类似Linux下的apt-get

**安装方法：**

- 方法一：
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- 方法二：
```
curl -LsSf http://github.com/mxcl/homebrew/tarball/master | sudo tar xvz -C/usr/local --strip 1
```

**例子：**

```
sudo brew install wget
sudo brew uninstall wget 
```

-------------------------------
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

- 方法一：
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
- 方法二：
```
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

**配置：**

1. 设置zsh为默认的shell，chsh -s /bin/zsh
2. 使用主题（推荐使用agnoster）
	- 下载agnoster主题，[下载地址](https://github.com/fcamblor/oh-my-zsh-agnoster-fcamblor)
	- 打开zsh的配置文件，vi ~/.zshrc
	- 修改ZSH_THEME的字段为agnoster，ZSH_THEME="agnoster"
3. 安装字体库
	- 下载字体库，[下载地址](https://github.com/powerline/fonts)
	- cd到文件目录，执行./install.sh
	- 设置字体，iterm2 -> profiles -> open profiles(或者直接cmd+o) -> edit profiles -> text -> change font，设置你喜欢的字体和大小即可
4. 配色（推荐使用Solarized）
	- 下载Solarized，[下载地址](https://github.com/altercation/solarized)
	- cd到solarized/iterm2-colors-solarized
	- 双击Solarized Dark.itermcolors和Solarized Light.itermcolors，导入iterm2
	- 设置配色，iterm2 -> profiles -> open profiles(或者直接cmd+o) -> edit profiles -> colors -> color presets -> Solarized Dark
5. 设置vim配色

	```
	$ cd solarized
	$ cd vim-colors-solarized/colors
	$ mkdir -p ~/.vim/colors
	$ cp solarized.vim ~/.vim/colors/
	```
	```
	$ vi ~/.vimrc
	syntax enable
	set background=dark
	colorscheme solarized
	```
6. 指令高亮
	- 下载zsh-syntax-highlighting，[下载地址](https://github.com/zsh-users/zsh-syntax-highlighting)
	- 移到zsh插件文件中，mv zsh-syntax-highlighting ~/.oh-my-zsh/custom/plugins/
	- 修改配置文件，vi ~/.zshrc，添加如下语句
	
		```
		plugins=(zsh-syntax-highlighting)
		source ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
		```
	- 执行source ~/.zshrc
	
-------------------------------