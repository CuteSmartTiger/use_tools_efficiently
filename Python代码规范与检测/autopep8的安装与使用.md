#### 1.1 cmd 命令下安装autopep8
```
 pip install autopep8
```

#### 1.2设置pycharm：
- File-->setting--> tools-->external tools
```Python
Name: autopep8
Program：autopep8

Parameters: --in-place --aggressive --aggressive $FilePath$
Working directory:$ProjectFileDir$
```

- Output Filters设置
```
name任意
regular expression to match output: $FILE_PATH$:$LINE$:$COLUMN$:.*
```




#### 其他设置

设置每行最长字符数为 79：
- File-Settings-Editor-Code Style-Right Margin
- 使用ctrl+alt+L 快捷键格式化代码  
- 运行tox命令检查，解决其他剩余问题
```
PS：pycharm默认就监测pep8代码格式，只是
提示是白色warn，隐藏在各种warn信息中，不
明显，大家可以把pep8的提示级别修改为 error：
 File-Settings-Editor-Inspection
```


#### Windows10
注意文件及其子文件的权限问题
- 目录及文件的命名问题，名字之间有空格则autopep8会提示报错，pylint则在cmd终端上运行命令
