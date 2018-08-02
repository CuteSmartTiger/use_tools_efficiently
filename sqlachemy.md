





- .更新数据
```
先查询
u=AlarmStatistical.query.first()
对象属性赋值
u.id=123  
#更新数据和变量赋值那么简单，但必须是通过查询返回的对象。
db.session.commit()
```
