## 语句与函数

与Java的区别是无（），无；

* ## 条件

  * ## if else
* ## 循环

  * ## while
  * ## for
  * ## 嵌套循环，debug打印

  注意：

  * 最好不要超过3个嵌套语句

  * break 中断循环语句

  * continue 继续，加快循环处理

* ## 异常

  异常捕获，防止程序终止运行，程序退出，控制台exit 0 是正常退出，非exit 0 是异常退出，服务断开

* 把异常捕获后，打印处理，让程序正常运行

* try对应某一行的异常

```
try:
  print "test"
expect:
    print "xxxx"
expect Exception as e:
    print "xxx"
else:
    print "no expection"
finally:
    print "all task will excute"
```

```
  重复的代码段

* def functionname (params):

  * retrun value

* 调用自带的函数

* 调用第三方模块函数

* 调用自定义的函数

  * 同模块

  * 不同模块

  * 不同包

* 函数注释在函数名的下面可以自动生成
```

注意  
1.注释函数  
'''  
'''  
2.return None 是return False  
3.import 模块（就是一个py文件），调用里面的方法  
4.调用包，python package（目录），并且带**init**.py文件，跨目录下进行调用  
5.sys.path对应的系统路径  
sys.path\[_module_\]._file_

```
* ## 参数传递

  缺省参数，默认参数

* def student\(age=1,name="hello"\):

  * statement
```

注意：

```
* 如果不传入参数，就使用默认的参数

* 一个函数可以有多个默认参数

* 默认参数只能放最后，不可以放中间和开头，除非无普通参数

## 不定长的函数

某些参数\*parameters,\*\*kwargs
```



```
def student(profile,*param_tuple):
    statement
```

1.\*param\_tuple 表示一个元组  
2.不定长参数放在普通参数后，除非无普通参数  
3.可以直接定义输入参数，是元组功能

```

```

def student\(profile,**kwargs\):  
        statement  
1.**kwargs 相等于一个字典，key=value方式传入参数  
2.不定长参数放后面，不可以放中间和开头  
3.直接定义输入参数是字典功能

```
元组格式 \(u"学生"，u"男性"，u”7岁“\)

def student\(profile,\(u"学生"，u"男性"，u”7岁“\)\)

def student\(profile,\*mytuple\)

例如：

查询页面，多个参数，设置不定长字段，接口函数，改动可以修改参数



* ## 匿名函数lambda 简单函数

#### 无名字的函数

#### 场景：

不想命名的函数，逻辑简单，一句话搞定

add=lambda x,y : x+y

x,y参数，x+y等于函数里的实现逻辑

## map

* map\(Fun,Seq\)
* 返回一个序列
* Fun是一个函数
* Seq是一个元组或列表

场景：

函数实现与返回的序列
```

def sqr\(x\)：  
    return x\*\*2

a=\[2,4,6\]

print map\(sqr,a\)  
\[sqr\(a\[0\]\)，sqr\(a\[1\]\),sqr\(a\[1\]\)\]  
\[4,8,36\]

```
## 方法

inputs = raw\_input\("please input that :"\)

## 场景

### 作业1

1.把1000-2500之间，既能被7整除，也能被5整除的数取出来， 放到一个列表输出

2.打印出0-20之间的数字，如果此数字能被3整除，输出英文”three”,如果能被5整除,输出”five”，如果既能被3整除也能被5整除，输出”threes+fives”,要求用到continue.

1 Threes 27 Threes... 4 14  fives Thees+fives
```

range\(0,10\),访问是0-9的数

list1 = \[\]  
for i in range\(1000,2501\) :  
    if i%7 == 0 and i%5 == 0:  
        list1.append\(i\)  
print\(list1\)

 

### 作业2

3.实现一个函数，要求对一个列表里面所有数字求和，如果里 面含有非数字的元素。直接跳过。比如\[1,2,3\]输出是5， 如果 是\[1,2,4,”a”\]输出是7。 并在另外一个包\(目录\)里面调用这个 函数

4.已有字典dic={“name”:”xiaozhang”,”sex”:”male”},访问字典dic\[“grade”\]， 通过try... exception把异常信息打印出来  
5.实现一个不定长参数的函数def flexible\(aa, \*args, \*\*kwargs\):， 把传入的参数和值打印出来。比如传入参数是  
flexible\(aa, 2, 3, x = 4, y = 5, \*\[1, 2, 3\], \*\*{'a':1,'b': 2}\)

输出结果:\(2, 3, 1, 2, 3\)，{'a': 1, 'y': 5, 'b': 2, 'x': 4}

