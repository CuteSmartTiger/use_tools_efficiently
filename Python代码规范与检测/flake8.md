##### 介绍
flake8是下面三个工具的封装：
1）PyFlakes
2）Pep8
3）NedBatchelder’s McCabe script

##### 安装
pip install flake8

##### pycharm配置详情:
```Python
Program: $PyInterpreterDirectory$/python
Arguments: -m flake8 --show-source --statistics $ProjectFileDir$
Working directory: $ProjectFileDir$
Output Filter: (留空就可以了, pycharm能自动识别路径.)



如果只想对当前文件进行检测则：
Arguments: -m flake8 --show-source --statistics $FilePath$
```
