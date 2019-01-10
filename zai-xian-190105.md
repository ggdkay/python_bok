## 在线

看别人的代码，更高效完全的测试用例

测试用例对比

单元测试拓展到自动化测试方面，包括：测试用例组织，测试数据方面使用

### unitest  python 的原生框架，最新的项目已发展到pytest

自动化测试的单元测试，最含金量高的测试

### 1.unittest单元测试用例对比

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

* py3 对比py2 高性能的库
* sys.version python 版本是多少
* py3 dict 返回的是列表，更新为迭代的对象，而且iteritems 无效函数，更改为items
* 注意求值得浮点时候，a//b 无余数，a/b 为浮点数
* py2 不定义encoding 会麻烦。网页或文件处理中文比较麻烦，依赖文件，网页，操作系统的
* py3 使用默认unicode 比较好改进，兼容各种编码，特别中文编码
* py3 open 打开文件，不用file
* py3 input 输入交互，不用raw\_input
* py3 range 范围，不用xrange 
* py3 subprocess 命令 执行，不使用commands



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



