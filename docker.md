#### docker
- daocloud 加速器
```
执行命令后记得配置文件中删除逗号
vi /etc/docker/daemon.json
```

- docker 镜像
```
查找相关镜像
docker search [image_name]

下载镜像
docker pull [image_name]

查看镜像
docker images

导出镜像
docker save [image_name] > [location_name]

导入镜像
docker load < [location_name]

删除镜像
docker rmi image_name

```

- docker 容器
```
启动镜像并创建出一个运行状态的容器
docker run -it --name contaioner_name image_name bash
-it 表示创建后进入容器的交互界面
--name 表示创建时容器的名称

启动镜像并创建容器时可以映射端口
docker run -it --name contaioner_name -p 9000:8080 -p 9001:8085 image_name bash
-p 9000:8080   将容器8080端口映射待宿主机9000端口

启动镜像并创建容器时可以映射容器文件到宿主机
docker run -it --name contaioner_name -v file_location:contaioner_file_location --privileged image_name bash
-v  将容器内部目录内容映射到宿主机目录下
--privileged  赋予最高权限


暂停容器
docker pause contaioner_name

恢复容器
docker unpause contaioner_name

停止
docker stop contaioner_name

启动
docker start -i contaioner_name

删除
docker rm contaioner_name
```


 - 查找docker中文件的路径
  ```
  touch [name]
  exit
  find /var/lib/ -name [name]
  ```
 - 其他
  ```
  fg   让后台的运行的程序到前台
  docker stop [docker_id]   停止进程
  docker kill [docker_id]   停止进程

  docker run 创建并启动一个容器，在run后面加上-d参数，则会创建一个守护式容器在后台运行。
  docker ps -a 查看已经创建的容器
  docker ps -s 查看已经启动的容器
  docker start con_name 启动容器名为con_name的容器
  docker stop con_name 停止容器名为con_name的容器
  docker rm con_name 删除容器名为con_name的容器
  docker rename old_name new_name 重命名一个容器
  docker attach con_name 将终端附着到正在运行的容器名为con_name的容器的终端上面去，
  前提是创建该容器时指定了相应的sh执行这个命令后，按下回车键，会进入容器的命令行Shell中。

  docker logs con_name 获取容器名为con_name的容器日志
  docker inspect 查看容器的详细信息
  docker top con_name 查看容器名为con_name的容器内部的进程
  docker exec 可以用来在容器中运行一个进程

  ```
