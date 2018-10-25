shell变量和一些编程语言不同，一般shell的变量赋值的时候不用带“$”，而使用或者输出的时候要带“$”。加减乘除的时候要加两层小括号。括号外面要有一个“$”，括号里面的变量可以不用“$”。需要注意的是，变量赋值，变量使用的时候不能有空格，否则会被解析成命令，报错无此命令


```
#!/bin/bash

a=10
b=20
c="this is a test"
d=$((a+b))
e=$((a-b))
f=$((a*b))
g=$((a/b))
h=$((a%b))
i=$((a**3))

echo $c
echo "a = "$a          #输出a的值
echo "b = "$b          #输出b的值
echo "a+b = "${d}      #输出a+b的值
echo "a-b = "${e}      #输出a-b的值
echo "a*b = "${f}      #输出a*b的值
echo "a/b = "${g}      #输出a/b的值
echo "a%b = "${h}      #输出a%b的值
echo "a^3 = "${i}     #输出a的3次方的值

echo "a+b = "$((a+b))  #输出a+b的值
echo "a-b = "$((a-b))  #输出a-b的值
echo "a*b = "$((a*b))  #输出a*b的值
echo "a/b = "$((a/b))  #输出a/b的值
echo "a%b = "$((a%b))  #输出a%b的值
echo "a^3 = "$((a**3)) #输出a的3次方的值

echo $((a+b*a-b/a+a%b+a**2)) #表达式可以很长

```
