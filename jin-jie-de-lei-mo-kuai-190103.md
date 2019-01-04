## 作业1

1.设计一个表示服务器的类。包含服务器的属性有:

• • • •

CPU个数， 内存大小， 磁盘空间大小

操作系统类型\(Linux, Windows\) 其中操作系统类型设置为私有变量，外部不可以更改。 实现一个方法，输出服务器的属性内容为以下格式:8核CPU，40G内存，150G磁盘空间，Linux

## 作业2

1.设计一个作业1中服务器的子类，实现一个新的方法，根据cpu个数，内存大小，磁盘空间大小计算出服务器当前价  
 格 ，计算公式为:CPU个数\* 1527.679+内存大小G \* 100.21+磁盘空间大小G \* 50.789。 返回数据类型为浮点型。 保留小数点后2位 。 并实例化此方法，打印出价格。



```
class ServerInfo():

    def __init__(self,cpu_nums=0,mem_size=0,disk_size=0):
        self.cpu_nums = cpu_nums
        self.mem_size = mem_size
        self.disk_size = disk_size
        self.__os_type = 'Linux'

    def getInfo(self):
        return (str(self.cpu_nums)+u"核CPU，"+\
            str(self.mem_size)+u"G内存，"+\
            str(self.disk_size)+u"G磁盘空间，"+\
            self.__os_type)

    def calcuServer(self):
        return round((int(self.cpu_nums)*1527.679+\
            int(self.mem_size)*100.21+\
            int(self.disk_size)*50.789),2)
```



