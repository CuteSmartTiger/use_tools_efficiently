条件判断中使用正则时需要使用双括号,正则表达式不可以加引号
```SHELL
#! /bin/bash
read -p "number" num
if [[ ! "$num" =~ ^[0-9]+$ ]];then
echo 'no number'
else
echo 'number'
fi
```


测试语法
sh -n test.sh
