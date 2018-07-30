#### docker
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
