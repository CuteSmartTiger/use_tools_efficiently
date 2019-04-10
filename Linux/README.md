#### 提高效率之工具


- 查看目录文件方面：
tree  

- 命令补全功能：
sudo apt-get -y install bash-completion  bash-completion-extras



统一整理后的脚本
```SHELL
#!/usr/bin/env bash


```


#### 命令相关
^


- 标准输出 重定向
```


```

-  shell脚本中运行python代码
```SHELL
#!/usr/bin/env bash
echo 'hello'

# 通过<<-将python语句重定向到/usr/bin/python执行
# EOF标记起始与结束的位置
/usr/bin/python <<-EOF
print 'excute python in shell scripts'
EOF  # <<后面添加-目的是结束位置的EOF前面可以有空格或tab键
```


- sed流编辑
```shell
# 查找匹配内容然后修改原文件
sed -i  s/localhost/127.0.0.1/g desktop.conf





```


- awk
```shell







```

- grep
```shell







```
