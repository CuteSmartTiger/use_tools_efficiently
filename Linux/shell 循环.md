### while 语句：条件为真才执行
- 格式：
```
while 条件
do
语句
done
```
注释：条件除了 while true 可以这样写，其它的条件都要用 test或者 []来判断


- 示例代码：
```
#!/bin/bash

i=$1
while [ $i -gt 0 ]
do
echo $i
i=$((i-1))
done
echo 'done'
```

补充解释：
```
-eq 等于
-ne 不等于
-gt 大于
-ge 大于等于
-lt 小于
-le 小于等于
```

### until语句:until语句是只要条件为假就执行下列语句
格式：
```
until 条件
do
语句
done
```

示例：
```
#!/bin/bash

i=$1
until [ $i -le 0 ]
do
echo $i
i=$((i-1))
done
```



### for语句
格式：
```
for 变量 in 列表
do
语句
done
```

示例：
```
#!/bin/bash
for i in `seq 2 8` #seq是一个命令，顺序生成一串数字或者字符
do
   echo $i
done
```
