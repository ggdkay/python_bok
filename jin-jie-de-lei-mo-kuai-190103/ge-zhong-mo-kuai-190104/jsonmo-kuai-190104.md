## json

```
• json.dumps: 将python对象（字典）转化【json字符串 】
• json.load: 将json字符串转化为【python对象】
```



```
dict = {"xx":"11","yy":“dd”}
json.dumps(dict,encoding='utf-8')


json_str = '{"xx":"11","yy":“dd”}'
json.loads(json_str,encoding='utf-8')
```







