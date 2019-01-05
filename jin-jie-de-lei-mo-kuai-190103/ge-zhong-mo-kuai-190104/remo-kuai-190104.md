## re 正则

```
re 模块常用方法:
• re.compile(pattern[, flags]) 把正则表达式语法转化成正
则表达式对象
• re.search(pattern, string[, flags]) 在整个字符串中查找匹配
正则表达式模式的位置，返回 MatchObject 的实例，如
果没有找到匹配的位置，则返回 None。
• re.match(pattern, string[, flags]) 在字符串的开始位置尝试
匹配正则表达式
• Re.findall() 显示出字符串中模式的所有匹配
```

简单操作，复杂逻辑

灵活，功能强大

可读性差



正则使用，在爬虫里面很好

pattern = re.compile\(r'\d+'\)

编译成Pattern对象，匹配文本，获得匹配结果，无则返回None

pattern.findall\('123jihvv'\) 从中查找数字



```
import re
pattern = re.compile(u'你好')
mm = pattern.match(u'时间')
if mm:
    match.group()
    

```





