## Ubuntu

### 搜狗输入法

1）官网下载http://pinyin.sogou.com/linux/?r=pinyin

2）16.04双击deb包安装可能会出现第三方支持的原因失败，选择命令安装

​       sudo dpkg -i input.deb，会显示有依赖，需要使用sudo apt-get install 依赖包（sudo apt-get -f install）

3）然后在language support把keyboard input method system改成fcitx

4）系统右上角会弹出键盘符号，点击搜索出搜狗输入法即可。

### TeamViewer

https://www.teamviewer.com/en/download/linux/

sudo dpkg -i input.deb安装，sudo apt-get -f install 解决依赖，然后再执行一边安装命令即可。

### chrome

http://www.ubuntuchrome.com/

chromium: Ubuntu Software

### anaconda

https://www.continuum.io/downloads#linux

bash Anaconda3-4.3.1-Linux-x86_64.sh 

### shadowsock-qt5

https://github.com/yangp725/tool/blob/master/shadowsocks/ubuntu.txt

### WPS

http://wps-community.org/downloads

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