# 理论还是基础

## 环境搭建

windows

* 配置window的路径

linux

* 安装pip

mac

    注意：
    pip仓库的地址 `pip.conf`
    pip.ini的配置

python 下载community 版本，免费

python 下载版本3.6

是否安装了对应的包

```
yum  list | grep -i pip
```

python 初始化，不需要指定数据类型

特殊的数据类型：字典，元组，列表

## Python基础数据类型

| 类型 | type | 例子 |
| :--- | :--- | :--- |
| 整数 | int | 1234,-10 |
| 长整型 | long | 10000000L |
| 浮点数 | float | 3.5 |
| 字符串 | string | hello python |
| 列表 | list | \["python",11,4.6\] |
| 元组 | tuple | \("straaa",1,2.4\) |
| 字典 | dictionary | {"name":"kay","sex":"F"} |
| 集合 | set | {1,2,4} |
| 布尔型 | bool | True,False |
|  |  |  |

### 不同类型转换

创建变量，需先定义变量类型

* 查看变量数据类型 type\(x\)

```
a=10
type(10)
<type 'int'>
```

* 字符串与整形互转
* 整形与浮点型互转
* 列表与元组互转
* 嵌套元组转字典

## 不同进制互转

|  | 2进制 | 8进制 | 10进制 | 16进行制 |
| :--- | :--- | :--- | :--- | :--- |
| 2进制 | - | bin\(int\(x,8\)\) | bin\(int\(x,10\)\) | bin\(int\(x,16\)\) |
| 8进制 | oct\(int\(x,2\)\) | - | oct\(int\(x,10\)\) | oct\(int\(x,16\)\) |
| 10进制 | int\(x,2\) | int\(x,8\) | - | int\(x,16\) |
| 16进制 | hex\(int\(x,2\)\) | hex\(int\(x,8\)\) | hex\(int\(x,10\)\) | - |

## 应用场景：

## 网络接口数据转换 bin2-&gt;int10

bin =&gt; 0b800

bin\(int\('9',10\)\)

==&gt; 0b1100

## 反馈

利用pip,安装第三方模块requests,描述你用什么方法来确认 安装是成功的。

1. 把2.918转化为整形

2. 把10进制数18转化为2进制数

3. 用java替换字符串:”Python is popular”里面的Python，并

   把java变换成JAVA

4. 把列表\[1, 2, 3,4 5,6,7,8\]里面的2, 4, 6,8打印出来

5. 创建一个字典，字典的key分别是name, sex, province ,修改

   原始province的值 为新值”江苏”

pip list \|grep requests 查看已经安装的包

int\(2.918\) 转换10进制

bin\(int\(18\)\)--&gt; 0b10010

判定是否in 存在Python,存在替换replace，JAVA

```
>>> s="Python is popular"
>>> s2=s.replace("Python","java")
>>> print s2
java is popular
>>> s2=s.replace("Python","java".upper())
>>> print s2
JAVA is popular
```

列表的等步长的打印，

```
>>> print ll[1::2]
[2, 4, 6, 8]
```

字典的增改，dict={},dict\["province"\]="test"

ss=u"江苏" 中文输出

xrange\(10\) 从0到10访问

len\(list\) list的长度

## 作业2

1. Test\_str=“Python was     created in 1989, Python is     using inAI, big data, IOT.”按下列要求对上面文字做出处理。  
   •把上面文字中的所有大写转化为小写，  
   •把这段话每个单词放到列表里面，不能不包含空格。

   •把列表最中间的一个单词打印出来。

疑问需求2！！

1. List1=\[“python”, 5,6, 8\], list2=\[“python”,”5”, 6, 8,10\],对list1和

   list2做出如下处理:

   * 把上面2个list的内容合并成一个

   * 利用set里面的方法，对合并后的list，去除重复元素。最

     后输出是还是list =\[“python”, 5,6, 8,”5”,10\] \(顺序可以不一

     样\)

   * 

```
>>> ll=List1+list2
>>> print ll
['python', 5, 6, 8, 'python', '5', 6, 8, 10]
>>> print set(ll)
set([5, 6, 'python', 10, 8, '5'])
```



