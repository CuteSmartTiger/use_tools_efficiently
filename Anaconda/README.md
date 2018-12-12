##### 查看conda信息
```
conda --version

conda info
```

##### 查看创建的虚拟环境
```
conda info -e
```
##### 创建新的虚拟环境
```
conda create --name pythontest python=3.6
```

##### 激活一个环境
```
windows:
activate pythontest

linux或mac
source activate pythontest
```
##### 退出一个环境
```PYTHON
windows:
deactivate

linux或mac
source deactivate
```

##### 删除一个环境
```
conda remove --name pythontest --all
```


##### 查看安装的包或者指定环境安装的包
```
conda list

conda list -n pythontest
```

##### 安装包
```
conda install package_name

```

##### 删除一个虚拟环境的包
```
conda remove -n pythontest package_name
```
