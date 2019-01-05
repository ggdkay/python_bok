## sys模块

```
sys 模块常用方法:
• sys.path 返回当前PYTHONPATH的列表
• sys.argv 获取命令行参数 0 代表自己，1 代表参数1，2代表参数2
• sys.exit 退出当前python进程
• sys.platform 获取当前系统平台，如:win32、Linux等
• sys.stdin 标准输入流，人机交互
• sys.stdout 标准输出流
• sys.stderr 标准错误流
```

## 场景

* 启动一个python脚本run.py,传入参数为/home/tools/src,把/home/tools/src加入到python path里面，打印出前后的pythopath列表信息。 如果此目录下没有任何py文件，程 序异常退出

* 把上面的脚本出信息通过sys.stdout重定向到log.txt



```
python run.py /test/123
sys.path.append(sys.argv)

sys.stdout > log.txt
```



