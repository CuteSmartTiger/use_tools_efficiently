#### 用户切换
"$"：普通用户提示符
"#"：root用户提示符

#### 修改普通用户用户名
su - 或 su - root（到root用户下。 注意要使用su -，原因见下文）
usermod  -l  新用户名  -d  /home/新用户名  -m  老用户名   

#### 修改密码
1. 修改普通用户密码
命令： sudo su        获取root权限
命令：passwd 用户名   如passwd wyc
输入两边新密码


2. 修改 root密码
命令：passwd  超级用户名    修改超级用户的密码，如root的密码
输入两遍新密码


#### 修改用户名
