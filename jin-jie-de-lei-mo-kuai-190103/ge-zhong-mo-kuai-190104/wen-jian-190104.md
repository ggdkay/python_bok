## 文件读写

open

Python3使用读写文件

#### 文件实例

file\_instance.read\(\) 一次性读取文件全部

file\_instance.readlines\(\) 一次性读全部，存列表，每行为一列表元素

file\_instance.readline\(\) 执行读一行

file\_instance.write\(\)写入文件，不换行

file\_instance.writelines\(\)把一个列表里面所有元素写入文件，不换行

file\_instance.flush\(\) 即时缓存数据输出到文件，不等关闭句柄

file\_instance.close\(\) 打开文件一定要关闭，不停打开不关闭会要一定限制影响

数据量大，中间遇到错误，前面的输出就不能看到，需调用flush,写入磁盘，也不能太频繁，影响读写速率

大文件只要某一行，linecache模块，linecache.get\(filename,行\)

## 注意：

```
1.file.open(encoding="utf-8") 读取有中文
```

## OS 模块

```
os.listdir() 罗列当前的所有目录
os.getcwd() 当前路径
os.stat(file) 文件大小，创建时间，最后的访问时间，创建备份文件，测试用例管理查询建立时间
os.chdir('/home/test') 改当前目录
os.system() 运行shell
os.path.join(path,name)连接目录与文件名
os.mkdir(name) 创建目录
os.path.basename(path) 返回文件名


os.stat(file) 最后访问时间
文件切割，文件备份，文件在写，不能备份
10分钟没继续在写，可以切割走

删除命令，一次性执行完退出
os.system('rm -f test.file')

linux/window的路径分隔符不一样
Linux '/'
window '\\'
获取文件的校验，可以兼容window,linux

os.path.exists('file')
os.path.basename('/path/name')
>> name 返回最后的文件名
os.path.isfile('/path/name')
>> True 是文件
>> False 不是文件

dir(os) 获取对应的方法列表
help(os.read())
```

## 场景

* 查找/tomcat/log/目录下的log文件，如果文件最后修改时间 是在1小时之前，把次文件打包压缩，备份到/home/back/log目录下

* 在Linux下每隔1分钟检查一下tomcat进程是不是在运行，如 果tomcat进程退出了，立即启动tomcat进程

* 搜索目录/home/tools/下所有已test开头，py结尾的文件\(包 括子目录的\),把文件全路径输出到一个列表里面打印出来

os.system\(\)

os.listdir\(\)

os.system\('ps \|grep 'Tomcat''\)



