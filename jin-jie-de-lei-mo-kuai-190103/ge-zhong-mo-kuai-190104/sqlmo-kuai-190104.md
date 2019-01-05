## mysqldb/pymysql

```
MySQLdb/pymysql常用方法:
• MySQLdb.connect 建立和MySQL 数据库的连接
• cursor=conn.cursor() 通过上一步建立的连接获取个cursor 对象
• cursor.execute(sql) 执行SQL 语句， 但返回结果不是SQL 执行的结果，是此SQL 执行后收影响的行数
• cursor.fetchall(): 获取SQL 执行的所有结果，返回 结果是个嵌套的元组
• cursor.fetchall()获取SQL 执行的结果，只获取第一条
connect.commit() 
• cursor.close() ， conn.close() : 关闭连接和cursor
```

## 场景

连接测试数据库，对其中某个表分别指向select, update, insert, delete语句





