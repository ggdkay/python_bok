## 不同字符串的变量访问与操作

```
s="hello python"
```

* 连接
* 复制
* 分割split
* 替换replace
* 字符串大小转换
* 字符的查找search

#### 常用的字符串方法

* decode

* encode

* startswith

* endswith

* len

* isdigit

* join

* strip

* index

* lower

## 场景

```
1.字符串的符号
str='' #单引号
str="" #双引号
str='''xxx
yy
zz''' # 三引号

2.复制多个符号
print "*"*100

3.字符串中有转义字符，需要转义，\\n,\\b
for item in path.split(";") :
    print item
切分window下的路径，获取对应的目录

4.split()默认空格拆分
5.截取后四位，list[-4:]
6.替换，ss="abc deg"
ss.replace("abc","123")

7.大写
love.upper()
love.lower()
8.首字母大写，capitalize()
9.startswith(),以什么字母开头
10.list每个元素以空格组合，"".join(list1)
11.查看字母的位置，ss.index('a') => 0
12.help(str) 查看具体的字符类型与用法
```



