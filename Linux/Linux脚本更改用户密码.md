echo "mytest" | passwd --stdin pi


echo "password" | passwd pi --stdin > /dev/null 2>&1






更改用户脚本的密码
echo pi:'test1234' |sudo chpasswd pi


echo cloud:'guyu8888' |sudo chpasswd cloud
