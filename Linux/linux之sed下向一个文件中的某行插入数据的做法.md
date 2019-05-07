sed -i 'ni\x' test.file        表示向test.file文件里的第n行的前面添加x内容

sed -i 'na\x' test.file       表示向test.file文件里的第n行的后面添加x内容

sed -i '/m/i\x' test.file     表示向test.file文件里匹配m字符串的行的前面添加x内容
sed -i '/m/a\x' test.file    表示向test.file文件里匹配m字符串的行的后面添加x内容

-i     表示in front，前面
-a    表示after，后面

比如向a.txt文件的首行添加123456789
# sed -i '1i\123456789' a.txt

比如向a.txt文件的第3行添加hhhhh
# sed -i '3a\hhhhh' a.txt

比如向a.txt文件匹配abcd字符串的行的前面添加66666
# sed -i '/abcd/i\66666' a.txt

比如向a.txt文件匹配1234字符串的行的后面添加hahaha
# sed -i '/1234/a\hahaha' a.txt

比如向/etc/puppet/puppet.conf文件中的第2行的前面添加" server=puppet01.test.cn"内容
然后再向第3行添加" runinterval = 600"内容
# /bin/sed -i '2i\ server=puppet01.test.cn' /etc/puppet/puppet.conf
# /bin/sed -i '3i\ runinterval = 600' /etc/puppet/puppet.conf
