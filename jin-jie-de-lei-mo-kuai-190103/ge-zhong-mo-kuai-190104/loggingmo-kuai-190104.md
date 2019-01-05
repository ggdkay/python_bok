## logging

```
logging.basicConfig 
•logging.basicConfig(filename="web.log", level=0,
format='%(asctime)s %(name)s %(levelname)s %(module)s:%(lineno)d %(message)s')

• logging.handlers.RotatingFileHandler: log文件到了一定大小自 动备份到一个新的文件
```

### 场景

在不同模块中输出log信息到同一个文件test.log上，要求log

输出不同级别的log， 包括输出异常信息到log文件



```
import logging
logging.getLogger(""模块).setLevel(logging.WARNING) 设置第三方级别高，不打印log
模块selenium,paramkio 等不想打印相关的log信息

定位格式，时间，行数
logging.basicConfig(filename="web.log",level=0,format='
    %(asctime)s %(name)s %(levelname)s %(module)s: %(lineno)d %(message)s')
    
log日志超过10M，就备份多个
log.exception

```



