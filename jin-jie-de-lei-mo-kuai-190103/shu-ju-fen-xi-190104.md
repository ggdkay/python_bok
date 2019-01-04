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
* 创建和共享程序文档

```
import numpy as np
%pylab inline
x = np.linspace(0,10) plt.plot(x,np.sin(x), x,np.cos(x))

```

## Pandas\(Python Data Analysis Library\)

* 一个专门应用大数据分析的包
* 应用金融行业的大数据分析
* 对于时间序列的数据分析（good at）
* 结构化的数据分析
* 基于Numpy ,底层计算密集型函数，由C开发
* http://odo.pydata.org/en/latest/perf.html
* 三种数据结构：Series,DataFrame,Panel,Panel4D

## 数据分析流程

数据源-数据清理-数据归集-数据可视化

## 场景

CPU趋势图

每月发布版本柱状图

Bug统计饼图

对美国共享单车数据分析





