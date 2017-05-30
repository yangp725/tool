[git-教程-lxf](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

生成SSH key:
ssh-keygen -t rsa -C "your email"

(ssh-keygen -t rsa -C "youremail@email.com" -f ~/.ssh/second)

 cat .ssh/id_rsa.pub 

然后将id_rsa.pub的内容拷贝到github

### 管理sshkey

https://www.zybuluo.com/yangfch3/note/172120

config文件

Host 192.168.1.96
Hostname 192.168.1.96
User yangpeng
Identityfile ~/.ssh/ip_id_rsa

Host 192.168.1.97
Hostname 192.168.1.97
User yangpeng
Identityfile ~/.ssh/ip_id_rsa

Host github.com
HostName github.com
User yangp725
IdentityFile ~/.ssh/id_rsa

测试连接github：ssh -T git@github.com