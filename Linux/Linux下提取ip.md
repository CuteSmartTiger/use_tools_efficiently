此方法获取的ip有端口  不推荐
ip address show dev eth0 | grep inet | grep  eth0 | awk '{ print $2 }'


用命令 “| sed‘s/^.*addr://g’”去除IP地址前面的内容:

用命令 “sed s/Bcast.*$//g”去除IP地址后面的内容:

较好的方法

ip=`ifconfig eth0 |grep 'inet addr' | awk '{print $2}' | sed s/^.*addr://g` && echo ${ip}

sed -n  '12,s/localnode=.*/localnode=${ip}/'p Makefile



sed  s/^localnode=.*/localnode=${ip}/g  Makefile
