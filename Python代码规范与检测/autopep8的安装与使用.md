#### cmd 命令下安装autopep8
```
 pip install autopep8
```

#### 设置pycharm：
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


#### pylint
```python
- program: python安装目录下scripts/pylint.exe
 - arguments: --output-format=parseable --disable=R -rn --msg-template="{abspath}:{line}: [{msg_id}({symbol}), {obj}] {msg}" $FilePath$
 - working firectory: $FileDir$
```


实际配置
```
D:\install software carefully\install documents\python\Scripts\pylint.exe

--output-format=parseable --disable=R --- disable=C0102,C0103,C0111,C0301,C0302,C0303,C0304,C0305,W0120,W0123,W0401,W0603,W0612,W0614,W0621,W0622,W0703,E1003,E1101 $FilePath$

```


#### 其他设置

设置每行最长字符数为 79：
- File-Settings-Editor-Code Style-Right Margin

- 使用ctrl+alt+L 快捷键格式化代码


- 运行tox命令检查，解决其他剩余问题
```
PS：pycharm默认就监测pep8代码格式，只是提示是白色warn，隐藏在各种warn信息中，不明显，大家可以把pep8的提示级别修改为 error：
 File-Settings-Editor-Inspection
```
