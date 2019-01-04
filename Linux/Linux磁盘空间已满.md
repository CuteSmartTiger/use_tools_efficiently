查看目录大小
du -sh /var/


du -sh : 查看当前目录总共占的容量。而不单独列出各子项占用的容量

du -lh --max-depth=1 : 查看当前目录下一级子文件和子目录占用的磁盘容量


查看容器日志
ls -lh $(find /var/lib/docker/containers/ -name *-json.log)
