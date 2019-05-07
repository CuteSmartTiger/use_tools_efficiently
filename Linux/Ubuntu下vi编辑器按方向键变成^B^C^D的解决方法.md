
#### 方法一：
vim /etc/resolv.conf
```
nameserver 8.8.8.8
nameserver 8.8.4.4
```

第一步. 执行命令(卸载vim-common)：
sudo apt-get remove vim-common -y
第二步. 执行命令(安装vim)：
sudo apt-get install vim -y



sudo apt-get remove vim-common -y
sudo apt-get install vim -y



#### 方法二：
方法2. 修改/etc/vim/vimrc.tiny文件，将set compatible改成set nocompatible，然后再添加一行set backspace=2即可
