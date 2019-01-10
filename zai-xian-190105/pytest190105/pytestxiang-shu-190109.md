## pytest 编写规范

* ![](/assets/import.png)



* 写法简单
* 不需继承
* 反馈的log报告结果也简单清晰，查看方便
* 需要注意的是pytest的tool需要替换unittest
* * tools =&gt; python Intefrated Tools =&gt; test runner =&gt; py.test
  * 

```
test_add.py

def add(x,y):
    return x+y

def test_add():
    assert add(1,2) == 3
```



##### sugar 进度

命令行输入

```
pytest -sq xx.py
```



#### 参数化

测试场景： 测试输入多个参数，登录成功，失败，多个账号（中，英）

```
import pytest
@pytest.mark.parametrize("x,y",[
    (3+4,7),
    (3+3,9),
    (3*4,9),
])
def test_add(x,y):
    assert x == y
```

json化文件输入



##### 多个assert （插件 python-assume）

* 多个断言条件，全部比较，尽管1，2错误，3正确，也会顺序比较

```
import time
import pytest
import pytest_assume

def add(x,y):
    return x+y
    

def test_add3():
    time.sleep(2)
    # pytest.assume()
    pytest.assume(add(1,5) == 1)
    pytest.assume(add(2,5) == 2)
    pytest.assume(add(3,5) == 8)
```

##### pytest-rerunfails

* 测试场景
  * 超时失败重试接口
  * web,app自动化的测试
* 解决？
  * 添加等待时间？
  * 重新执行？

```
pytest -sq --reruns 3 xx.py 即可
```

##### pytest-ordering

* 测试场景
  * web测试，上下测试用例切换页面依赖关系
  * 修改信息的页面中，依赖于前面用例创建信息，比如修改账号信息，依赖已经创建好的数据
  * 

```
 
import time
import pytest

value = 0

def add(x,y):
    return x+y

@pytest.mark.run(order=2) ## 修饰符
def test_add2():

    print("random_value 111==> ")
    time.sleep(3)
    assert  value == 10

@pytest.mark.run(order=1)
def test_add1():
    global value
    value = 10

    print("random_value 222==> ")
    assert value == 10
```



