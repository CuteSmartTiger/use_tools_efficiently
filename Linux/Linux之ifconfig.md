```
[root@www ~]# ifconfig {interface} {up,down}  #观察与启动接口
[root@www ~]# ifconfig interface {options}    #设定与修改接口
选项与参数：
interface：网络卡接口代号，包括 eth0, eth1等
options  ：可以接的参数，包括如下：
up, down ：启动 (up) 关闭 (down)
mtu      ：可以设定不同的 MTU 数值，例如 mtu 1500 (单位为 byte)
netmask  ：子网掩码；
broadcast：广播地址

[root@www ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 08:00:27:71:85:BD
      inet addr:192.168.1.100  Bcast:192.168.1.255  Mask:255.255.255.0
      inet6 addr: fe80::a00:27ff:fe71:85bd/64 Scope:Link
      UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
      RX packets:2555 errors:0 dropped:0 overruns:0 frame:0
      TX packets:70 errors:0 dropped:0 overruns:0 carrier:0
      collisions:0 txqueuelen:1000
      RX bytes:239892 (234.2 KiB)  TX bytes:11153 (10.8 KiB)

      # eth0：网卡名称
      # HWaddr：网卡的硬件地址，俗称的MAC地址
      # inet addr：IPv4 的IP地址，后续的Bcast,Mask分别代表的是广播地址与子网掩码
      # inet6 addr：是IPv6的版本的IP
      # MTU：网络最大传输单元
      # RX：那一行代表的是网络由启动到目前为止的封包接收情况,packets 代表封包数、errors代表封包发生错误的数量、dropped代表封包由于有问题而遭丢弃的数量
      # TX：与 RX 相反,为网络由启动到目前为止的传送情况；
      # collisions：代表封包碰撞的情况,如果发生太多次,表明网络状况不太好
      # txqueuelen：传输数据的缓冲区的储存长度
      # RX bytes, TX bytes：总接收、发送字节总量

[root@www ~]# ifconfig eth0 192.168.100.100
# 设置eth0的ip地址为192.168.100.100

[root@www ~]# ifconfig eth0 192.168.100.100
netmask  255.255.255.0 mtu 8000
#设置eth0的ip地址,子网掩码，mtu

[root@www ~]# ifconfig eth0:0 192.168.50.50/24
[root@www ~]# ifconfig eth0:0 192.168.50.51/24
#在eth0网卡上再配置两个ip，相当于虚拟两个网络接口

[root@www ~]# ifconfig eth0 down
# 关闭网卡eth0

[root@www ~]# ifconfig eth0 up
# 启动网卡eth0
```


#### ifup和ifdown 与 ifconfig 网卡名 {up, down}等价
```
[root@www ~]# ifup eth0
# 启动网卡eth0
[root@www ~]# ifconfig eth0 down
# 关闭网卡eth0
```
