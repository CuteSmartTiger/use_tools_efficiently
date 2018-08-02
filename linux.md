### 网络相关


####  route 命令添加路由信息
***注意，使用route 命令添加的路由，机器重启或网卡重启后路由会失效***
```
查看路由
route

添加默认网关
route add default gw ip

删除默认网关
route del default gw ip

```
- 待理解
```
//添加到主机的路由
# route add –host 192.168.1.11 dev eth0
# route add –host 192.168.1.12 gw 192.168.1.1
//添加到网络的路由
# route add –net 192.168.1.11 netmask 255.255.255.0 eth0
# route add –net 192.168.1.11 netmask 255.255.255.0 gw 192.168.1.1
# route add –net 192.168.1.0/24 eth1
//删除路由
# route del –host 192.168.1.11 dev eth0
```


#### 输入命令
```
history    查看历史输入记录
```

  - 用putty操作进入虚拟环境
  ```
  docker  ps -a
  docker  ps -s
  docker exec -it [contaioner_name]
  source flask/bin/activate
  ```
   - putty效率
  ```
  善于用table键
  多开几个putty窗口  进入不同容器进行查看或其他操作
  ```


  - 日志相关
  ```
  vi /var/log/vdidesktop/vdidesktop.log        查看日志
  tail -f  filename                            监听文件最后几行
  ```
