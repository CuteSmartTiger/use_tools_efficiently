#### 2.1 pylint
```Python
pip install pylint
```
```python
- program: python安装目录下scripts/pylint.exe
- arguments: --output-format=parseable --disable=R -rn --msg-template="{abspath}:{line}: [{msg_id}({symbol}), {obj}] {msg}" $FilePath$
 - working firectory: $FileDir$
```


实际配置
```
D:\install software carefully\install documents\python\Scripts\pylint.exe

--output-format=parseable --disable=R --- disable=C0102,C0103,C0111,C0301,C0302,C0303,C0304,C0305,W0120,W0123,W0401,W0603,W0612,W0614,W0621,W0622,W0703,E1003,E1101 $FilePath$
- working firectory: $FileDir$
```
