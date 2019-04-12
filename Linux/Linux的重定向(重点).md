- [Linux 输入输出重定向 2>/dev/null和>/dev/null 2>&1和2>&1>/dev/nul](https://blog.csdn.net/freeking101/article/details/81212207)


当执行shell命令时，会默认打开3个文件，每个文件有对应的文件描述符来方便我们使用：
类型	文件描述符	默认情况	对应文件句柄位置
标准输入（standard input）	0	从键盘获得输入	/proc/slef/fd/0
标准输出（standard output）	1	输出到屏幕（即控制台）	/proc/slef/fd/1
错误输出（error output）	2	输出到屏幕（即控制台）	/proc/slef/fd/2


在工作中用到最多的就是nohup command >/dev/null 2>&1 &命令
