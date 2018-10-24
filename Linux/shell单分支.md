格式：
```
if 条件 ;
then
结果
fi
```
补充：最后面一定要有fi，在shell脚本里面，控制分支结构结束都要和开头的单词相反，例如，if <–> fi，case <–> esac。

示例：
```
#!/bin/bash

echo "Please input a filename"

#读取输入的文件名，然后检测当前目录下的filename的类型
read filename
if [ -f $filename ];then
echo "this file is a ordinary file."
fi

```
