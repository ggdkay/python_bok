## 数据分析

anaconda工具管理

Jupyter

Pandas

Pandas读取CSV文件

Pandas画折线图

Pandas读写Excel文件

Pandas画饼图

## 一句话的简述

### anaconda 是一个软件集成包，上百个科学计算包及其依赖

安装

* conda --version
* conda list

## Jupyter

Jupyter Notebook

* 一web 应用程序
* 可以在线写代码，实时数据可视化
* 创建和共享程序文档，markdown 格式

```
import numpy as np
%pylab inline
x = np.linspace(0,10) plt.plot(x,np.sin(x), x,np.cos(x))
```

docker 安装，即可快速启动

## Pandas\(Python Data Analysis Library\)

* 一个专门应用大数据分析的包
* 应用金融行业的大数据分析
* 对于时间序列的数据分析（good at）
* 结构化的数据分析
* 基于Numpy ,底层计算密集型函数，由C开发
* [http://odo.pydata.org/en/latest/perf.html](http://odo.pydata.org/en/latest/perf.html)
* 三种数据结构：Series,DataFrame,Panel,Panel4D
* 集成mathlab 的库



## Pandas优势：可读性，方便有表格

量化分析，股票分析，支持Python，大数据分析（load内存）快，时间序列分析

odo-性能问题优势：csv-pg

read 30M /s,write 150M/s

## 

## 数据分析流程

### 数据源-数据清理-数据归集-数据可视化

## 主要：数据清理，数据归集

### 出成绩：数据可视化

```
文件flush 立即写数据到文本中，不会丢数据，工作效率更高

sar 5秒取CPU的趋势图数据，横坐标是时间，竖坐标是CPU的值
time,user,system,usage
1.先做数据分析，需求分析
2.图密集少取点，有序波动，波峰波谷
3.监控进程的CPU的百分率，整体程序，某个进程的CPU利用
4.字符串时间分解对象，datetime

```

## 场景

CPU趋势图

每月发布版本柱状图

Bug统计饼图

对美国共享单车数据分析



## 管理职位的mysql的bug（代码）

1.饼图的bug的数据与占比率

2.版本的bug的发布次数

3.CPU的趋势图

4.短信的计费系统700多行，每秒1万多条

## 代码分析

转换对象

字符串出现最多，python.counter\(\)





