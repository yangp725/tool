## Ubuntu

### 初始

sudo apt-get install git vim g++ wget terminator

### terminator

http://blog.wentong.me/2014/05/work-with-terminator/

http://woshijpf.github.io/2016/04/18/Terminator/

配置文件（可以使用man terminator_config查看）：vim ~/.config/terminator/config

cursor shape, (Menu->Edit->Profile Preferences->General Tab -> "Cursor Shape" and "I beam")

color table, http://www.sioe.cn/yingyong/yanse-rgb-16/

### 搜狗输入法(不要用！)

1）官网下载http://pinyin.sogou.com/linux/?r=pinyin

2）16.04双击deb包安装可能会出现第三方支持的原因失败，选择命令安装

​       sudo dpkg -i input.deb，会显示有依赖，需要使用sudo apt-get install 依赖包（sudo apt-get -f install）

3）然后在language support把keyboard input method system改成fcitx

4）系统右上角会弹出键盘符号，点击搜索出搜狗输入法即可。

*卸载：*http://codepub.cn/2015/11/27/Ubuntu14-10-install-and-uninstall-sogou-input-method/

> 命令查看下安装的搜狗拼音输入法 sudo dpkg -l so*
>
> 然后卸载搜狗拼音 sudo apt-get purge sogoupinyin

### google 拼音

sudo apt-get install fcitx-googlepinyin

### TeamViewer

https://www.teamviewer.com/en/download/linux/

sudo dpkg -i input.deb安装，sudo apt-get -f install 解决依赖，然后再执行一边安装命令即可。

### chrome

http://www.ubuntuchrome.com/

chromium: Ubuntu Software

### anaconda

https://www.continuum.io/downloads#linux OR https://repo.continuum.io/archive/index.html

bash Anaconda3-4.3.1-Linux-x86_64.sh 

修改zsh设置：

vim ~/.zshrc，要将.bashrc中的一些设置加入其中

> PATH="\$PATH:$HOME/anaconda3/bin:/usr/bin:/bin:/usr/sbin:/sbin"

source ~/.zshrc

### shadowsock-qt5

https://github.com/yangp725/tool/blob/master/shadowsocks/ubuntu.txt

### WPS

64位安装后无法打开, 使用32位版本, 

> http://community.wps.cn/download/

> http://kdl.cc.ksosoft.com/wps-community/download/a21/wps-office_10.1.0.5672~a21_i386.deb

### server

生成公钥私钥 ssh-keygen -b  2048

公钥拷贝 cat ~/.ssh/id_rsa.pub 

### Typora

https://typora.io/#linux

1)optional, but recommended

sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE

2)add Typora's repository

sudo add-apt-repository 'deb https://typora.io ./linux/'
sudo apt-get update

3)install typora

sudo apt-get install typora

### 修改pip下载源

https://segmentfault.com/a/1190000006111096

在pip install的最后加上 

> -i https://pypi.tuna.tsinghua.edu.cn/simple   (清华源)

> -i https://pypi.douban.com/simple (豆瓣源)

vi ~/.pip/pip.conf

```
 [global]
 trusted-host =  mirrors.aliyun.com
 index-url = http://mirrors.aliyun.com/pypi/simple
```



### ZSH

> sudo apt-get install zsh
>
> wget --no-check-certificate [https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh](https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh) -O - | sh
>
> chsh -s /bin/zsh
>
> reboot or re-login # or reopen the terminator

### torch

https://pytorch.org/

下载wheel文件使用pip安装（注意：不能修改wheel文件名）

### screen

https://www.vultr.com/docs/using-screen-on-ubuntu-14-04

### 虚拟环境

（http://virtualenvwrapper.readthedocs.io/en/latest/install.html）

(http://pythonguidecn.readthedocs.io/zh/latest/dev/virtualenvs.html)

> pip install virtualenvwrapper / pip install --user virtualenvwrapper  

然后修改.bahrc

> export WORKON_HOME=$HOME/.virtualenvs
> export PROJECT_HOME=$HOME/Devel
> source /home/yangpeng/.local/bin/virtualenvwrapper.sh	

重新进入terminal，

> mkvirtualenv -p /usr/bin/python py2_yp
>
> mkvirtualenv -p /usr/local/bin/python3 py2_yp

> workon py2_yp （进入）

> deactivate (退出)

在虚拟环境中，不使用sudo权限就可以把包安装在虚拟环境中了。



## ubuntu onedrive

https://linux.cn/article-3362-1.html

https://github.com/xybu/onedrive-d-old

> git clone https://github.com/xybu92/onedrive-d.git
>
> cd onedrive-d
>
> ./install.sh

运行 onedrive-pref 进行配置https://github.com/xybu/onedrive-d-old/issues/134

运行 onedrive-d start 启动