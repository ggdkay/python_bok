## 测试初始化

### setup,teardown

list\(range\(10\)\) 创建0-9的列表

list.pop弹出最后一个

### 不同级别的用例

* method

setup,teardown 执行用例前进行环境启动，执行完毕清楚脏数据

* class

执行所有的方法执行一次,多个用户，多个登录与退出函数，不值得，所以抽象一个函数

* module

所有类执行一次，登录一次所有的测试方法都用同一个session

### 测试报告：Htmlesrunner

对应的是所有的字节流进行保存

* 测试类，每次执行一次test\_xx测试方法，都会执行一次setup,teartdown

##### teardown

```
import unittest

class simple_test(unittest.TestCase):
    def setUp(self):
        print("methid 11")
        self.foo = list(range(10))
        print(self.foo)

    def test_1st(self):
        print("test_1st")
        self.assertEqual(self.foo.pop(),9)

    def test_2st(self):
        print("test_2st")
        self.assertEqual(self.foo.pop(),8)

    def tearDown(self):
        print("tearDown end")


if __name__ == '__main__':
    unittest.main()
```

##### - 执行两次 teardown,每个test\_xx方法使用一次，数据校验一致都是9

##### teardownclass

```
import unittest

class simple_test(unittest.TestCase):
    @classmethod  ## 修饰符要加
    def setUpClass(self):
        print("methid setup")
        self.foo = list(range(10))
        print(self.foo)

    def test_1st(self):
        print("test_1st")
        self.assertEqual(self.foo.pop(),9)

    def test_2st(self):
        print("test_2st")
        self.assertEqual(self.foo.pop(),8)

    @classmethod
    def tearDownClass(self):
        print("tearDown end")


if __name__ == '__main__':
    unittest.main()
```

* 结果，使用classmetod 可持续使用结果，不需要每个此时方法重置数据
* 例如：切换页面，值不变，可以传递到第二个页面进行赋值

##### teardownModule

```
import unittest

def setUpModule():
    print("tearDown setip")
    global foo   ## 定义global foo 
    foo = list(range(10)) 


class simple_test1(unittest.TestCase):

    def test_1st(self):
        print("test_1st")
        self.assertEqual(foo.pop(),9) ## 定义 foo 持续使用

    def test_2st(self):
        print("test_2st")
        self.assertEqual(foo.pop(),8)## 定义 foo 持续使用


class simple_test2(unittest.TestCase):

    def test_1st(self):
        print("test_1st")
        self.assertEqual(foo.pop(), 7)## 定义 foo 持续使用

    def test_2st(self):
        print("test_2st")
        self.assertEqual(foo.pop(), 6)## 定义 foo 持续使用


def tearDownModule():
    print("tearDown end")


if __name__ == '__main__':
    unittest.main()
```

* 比class 级别，可以跨多个类使用
* 


