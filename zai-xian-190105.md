## 在线

看别人的代码，更高效完全的测试用例

测试用例对比

### 1.单元测试用例对比

* 语句（多个条件or的覆盖不断） &lt; 条件 （用例覆盖多，但是需要删减）

路径覆盖

对于不同的测试，先有测试文档，再有测试代码

例如：

* 测试登录模块，不同逻辑里面不同的代码逻辑

### 2.py2与py3的代码对比

1. [http://www.runoob.com/python/python-2x-3x.html](http://www.runoob.com/python/python-2x-3x.html)

   ![](/assets/import_py2_3.png)

编码方式：ASCII 系统默认的编码，Python3的默认编码

coder.open\(encoding='utf-8'\)

### 2.unittest 与规范

![](/assets/unit test.png)

PEP8 的Python代码的规范，加强容错和可读性

```
import unittest

def add(x,y):
    return x+y
    
class TAdd(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(1,3),4)
        
    def test_add2(self):
        self.assertEqual(add(1,3),1)


```

```
1.run 执行，识别到unittest,因为是import对应的包名。
```

```
2.子类继承子类的方法，传入TestCase类

3.编写成功失败的用例！！
```



