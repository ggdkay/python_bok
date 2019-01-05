## command&subprocess

```
commands 模块常用方法:
Commands一般用在liunx

• commands.getoutput(command): 获取命令执行后的输
出结果
• commands.getstatus(command): 获取命令执行后的返
回的状态码
• commands.getstatusoutput(command):返回一个元组，
    第一个元素是状态码，第二个元素是输出结果
```

```
subprocess模块常用方法:
可用在windows和Linux

• subprocess.call(command,shell=Ture): 执行windows下命令
，返回执行执行状态结果
• Subprocess.check_call(command,shell=Ture): 执行windows
    下命令，返回执行执行状态结果
• Subprocess. check_output(command,shell=Ture): 返回执行
命令后的输出
```

### 场景

1.通过windows下ping命令， 得出www.testerhome.com的服务器IP地址

2.通过python启动一个windows应用程序

3.在Linux下启动tomcat进程，并判断tomcat启动是否成功

```
import subprocess,re
# # subprocess.call("ifconfig")
print("*"*100)
# subprocess.check_call("ifconfig",shell=True)
ss = subprocess.call("ping www.testerhome.com",shell=True)


判断是否启动成功，window三方api可以调用
进程是否启动成功
ss = subprocess.call("python *.exe",shell=True) ??



```



