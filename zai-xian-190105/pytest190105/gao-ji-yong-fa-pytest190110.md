## pytest 高级用法，自定义Marks

* 测试场景
  * 系统的测试用例千个，每次发版执行来不及
  * 通过关键字运行测试用例 pytest -k 
    * 缺陷，难以维护，无法多重达标
  * 通过标签来运行测试用例，既可以用于函数，也可是作用于类
* 
```
@pytest.fixture 有不同的级别可以调试，fuction,class,session,package 
```

module 模块执行一次，通常是setup,teardown

*  导航栏用户的删除和增加，可以当导航为一个模块

class 对应的类执行一次，可以设置自动执行，不需在类中每一个方法备注

 

##### fixtures 中的装饰器使用

yield􏰆􏰯􏰀􏰉􏰛 前 相当于setup 

yield 􏰆􏰣􏰀􏰉后 相当于􏰛tearDown

##### fixture 多种不同的调用方式

* 直接函数名
* 使用usefixtures decorateor
* 使用autouse

```
import pytest

@pytest.fixture(scope='module', autouse=True)
def loginout():
    print(" in ")
    yield
    print(" out ")

@pytest.fixture(scope='class',autouse=True)
def lll():
    print("xxxx")

class TestSample():

    def test_ans(self):
        print("I am TestSample1 ==1 ")
        assert 1+2 == 3


    def test_ans1(self):
        print("I am TestSample1 == 2 ")
        assert  1+3 == 4

class TestSample2():

    def test_ans2(self):
        print("I am TestSample2")
        assert  1+3 == 4


class TestSample3():

    def test_ans3(self):
        print("I am TestSample3")
        assert  1+3 == 4
```

##### conftest.py

* 共享定义的fixture;
* 放在testcases目录下，每个子目录都可以存在conftest.py
* 子目录下的conftest.py中的fixture优先

##### 场景：

修改一个开始连接数据库类似的函数，不需要每个函数都需要修改，统一在conftest.py 定义修改即可,conftest.py 定义在父目录中

```
import pytest

@pytest.fixture(scope='session',autouse=True)
def build_db_connect():
    print("db build connection")
    yield
    print("db close connection")
```

##### 标签记录

统计测试用例的编写人，-m

统计测试编写的用例通过率

统计关键用例P1

统计语法类似于python 

```
pytest -sq  xx.py -m 'not tan'
```

pytest -sq xx.py -m 'tan' or -m 'P1'

```
    @pytest.mark.tan
    @pytest.mark.P1
    @pytest.mark.usefixtures('loginout')
    def test_ans(self):
        print("I am TestSample1 ==1 ")
        assert 1+2 == 3
```

#### python 调用执行命令行

执行module

```
pytest -v xx文件
```

执行类，方法

```
pytest - v xx文件::类
pytest - v xx文件::类:: 方法
```



执行目录或package

```
pytest -v xx目录
```



执行标签

```
pytest -m P0 xx目录
```



#### 执行方式2

pytest.main 参数与pytest 命令行





