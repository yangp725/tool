### Anaconda
https://www.continuum.io/downloads#linux

修改路径vim .bashrc
export PATH="/home/yp/anaconda3/bin:$PATH"

保存
source .bashrc


###服务器-本地浏览器：

服务器输入 ipython notebook --ip=172.18.217.88 --port=8800 --no-browser

然后在本地浏览器输入172.18.217.88:8800即可！

### 服务器端配置：

http://blog.leanote.com/post/jevonswang/%E8%BF%9C%E7%A8%8B%E8%AE%BF%E9%97%AEjupyter-notebook

ssh到服务器

1.生成配置文件
'''
jupyter notebook --generate-config
'''
2.在terminal打开ipython，生成密码明文
'''
from notebook.auth import passwd
passwd()
'''

3.修改配置文件

vim ~/.jupyter/jupyter_notebook_config.py
'''
c.NotebookApp.ip='*'
c.NotebookApp.password = u'sha1:e88109549gtb:74f330f22223608e137169d09eb82d5f1d03fe3d'
c.NotebookApp.open_browser = False
c.NotebookApp.port = 8888
'''
加入上边代码，修改psw和port

4.启动，jupyter notebook， 这时候就不用配置ip和port了

5.远程访问，从本地浏览器直接访问`http://address_of_remote:8888`

如果访问失败，有可能是防火墙问题。建立ssh通道，在本地终端中输入

`ssh username@address_of_remote -L127.0.0.1:1234:127.0.0.1:8888` 
便可以在`localhost:1234`直接访问远程的jupyter了。
