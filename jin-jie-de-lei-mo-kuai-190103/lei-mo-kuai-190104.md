## 类，模块

面向对象思想

类，模块，包

类，构造函数

self的定义，类变量，实例变量

访问类的函数，属性

变量作用域，下划线的含义

类的继承，访问父类

静态方法，类方法

装饰器（好用的语法糖）

自定义Python包

## 面向对象

* 数据，属性
* 方法

对象是实例化，类是共同模抽象出来的多方法

## 构造函数

\_\_init\_\_\(self\)

默认构造函数无法传参

可以通过get,set方法设置

## 模块

一个文件 xx.py

## 包

有_init_.py文件，就可以被其他模块导入调用此包里面 的任意文件（模块）

self.name 实例对象

## super 初始化对象\_\_init\_\_\(self,...\)

继承：基于共同的属性，衍生其他的属性或方法

```
class Person(Object):
    xxx
class Student(Person):
    def __init__():
        super(Person,xx) 

# 1.super需要父类有传参Object,python3不需要        
2.在子类Student里面找不到方法，就访问父类的实现的方法
```

## 继承

多重继承，会初始化函数，\_\__init_\_\_\(\)

属性，方法增加

## 多态

重写父类

场景：

发送对象的不同，调用的方式不同，允许不同类的对象对同一消息做出响应

**多态的作用**

消除类型之间的耦合关系

场景：

快捷键，不同应用的同一个按键的快捷方式

```
*.在子类Student里面找不到方法，就访问父类的实现的方法
```

## 静态与普通类方法差异

不需要实例化,就可以调用

```
场景，共享共用，不需实例
```

```
@staticmethod
def test():
    print xx

@classmethod 类方法，一般传递cls
def test2(cls):
    print xx
```

```
@proterty
def test(self):
 print xx 

 使用调用不需要小括号
 a.test
```

## 下划线，双下划线，

\_\_ 开头是私有变量或方法，private,属性不可被外部访问，get，set访问

\_开头，可以被外部访问，不能随意调用

\_\__xx_\_\_ 初始化的方法名，系统调用

## 装饰器

```
@contexmanager
def test():
     xx

def contextmanager():
     xxx

调用函数
```

## 应用场景：

计数函数耗费时间,不需要每个函数都写对应的计算时间

需要传入一个函数，然后调用该函数！！！

#### 日志logging

#### auth鉴权

```
def time_count(func):
  def wrap(*args,**kwargs):
    tmp_res=func(*args,**kwargs)
    print "time cost:",time.time()-time_flag
    return tmp_res
  return wrap


可以多个修饰器
@login
@time_count
def loop_time(x,y):
  print xx

转变为多个方法调用
login(time_count(log_time(x,y)))

console:
time cost:1.8xxx
time cost:1.3xxx
```



