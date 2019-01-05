## time

```
time 模块常用方法:
• time.time() 获取1970.1.1.0:0:0 到当前的时间
• time.localtime(): 获取本地时间
• time.gmtime(): 获取格里尼治时间
• time.strftime(): 格式化时间格式
• time.strptime():字符串时间格式转化为时间
• time.mktime(): 将时间元组转换为1970/1/1 0:0:0 到目
前的时间值
• datetime.timedelta: 计算两个datetime对象的时间差
```

## 场景

在web性能测试中，我们经常需要度量一个transaction\(事务\) 需要花费多长时间，通常开发人员会使用log4j打印出事物的开 始点和结束点。下面是个真实的log4j输出内容

DEBUG 180106 21:58:51,607Receiver\_1\#receive a new request, the session id is 2018010610020809

。。。  
计算出处理这个事务所花费的时间

```
import time,sys

time.strftime("%Y-%m-%d %H:%M") 2018
time.strftime("%y-%m-%d %H:%M")   18

time.strptime("%Y-%m-%d %H:%M:%S %Z") zone 时区

sys.setdefaultencoding("utf-8")

time.localtime() # 当地时间
time.gmtime() # 国际时间，统一时间

time_delta() 时间差
datetime.strptime(''对象,''格式化)
```



