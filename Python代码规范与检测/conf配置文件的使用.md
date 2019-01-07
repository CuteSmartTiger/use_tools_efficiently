
#### 基本操作
```python
创建ConfigParser实例
config=ConfigParser.ConfigParser()

读取配置文件
config.read(filename)

返回某个项目中的所有键的序列
config.options(section)

返回section中的option的键值
config.get(section,option)

添加一个配置文件的section节点
config.add_section(section-name)

设置某个section中键名为option的值
config.set(section,option,val)

返回配置文件中所有的section
config.section()

写入配置文件
config.write(obj_file)

```
#### 示例
  ```Python
  #-*- coding: utf-8 -*-
  import ConfigParser


  def func():
      cp = ConfigParser.SafeConfigParser()
      cp.read('kuaidaili_spider.cfg')

      print 'mongodb host',cp.get('mongodb','host')
      print 'kafka bootstrap_servers',cp.get('kafka','bootstrap_servers')
      print 'log file name',cp.get('log','log_file_name')
      print 'zookeeper conn string',cp.get('zookeeper','conn_str')

  if __name__ == '__main__':
      func()
  ```




#### 如果有中文则写法如下
```

[msg]
hello = 你好
config_parser_unicode.py


import ConfigParser
import codecs

cp = ConfigParser.SafeConfigParser()
with codecs.open('myapp.conf', 'r', encoding='utf-8') as f:
    cp.readfp(f)

print cp.get('msg', 'hello')

```


#### 参考文章

- [Python中配置文件的使用](https://blog.csdn.net/mrbcy/article/details/60143067)
