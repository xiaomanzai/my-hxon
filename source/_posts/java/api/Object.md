---
title: object
category: java api
tags:
  - java
date: 2023-11-02 17:24:45
---
只有无参构造，作为顶级后类，所有的方法都继承于 object

![image.png](https://s2.loli.net/2023/10/21/o35sRu6ClpAMhPi.png)


![image.png](https://s2.loli.net/2023/10/21/WsPSwIRxbFlAajg.png)

tostring 的底层
全类名 + @ + 地址名


## system. out. println  

system 类名
out 静态变量
out 是 printstream 流
system. out 获取打印变量

底层会调用 String. valueOf 来调用 object tostring 方法。
然后再调用 wrintLn 来输出和换行

因此对于一般类重写要重写 tosring 方法

## equals 方法

就是比较属性值
首先比较地址，后面比较成员属性值是否相等

对于 string
先比较是否是字符串，再比较内容

## clone

对象克隆：把 a 对象的属性值完全拷贝给 b 对象

clone 是 protected 只能被本包和子类调用
因此 clone 方法必须被重写

调用父类的方法 super. clone

本类还要实现 cloneable 作为标记接口

#### 浅拷贝
对于直接拷贝类型，直接类型直接 copy ，引用类型直接 copy 地址值


#### 深克隆

基本数据类型会直接拷贝，而对于引用数据类型则会再堆内存创建新的地址，而对于字符串因为字符串的地址管理再串池因此则会直接从串池引用归来，因此地址值不变

深克隆则需要重写

[![深克隆](https://z1.ax1x.com/2023/11/05/piQHukj.png)]( https://imgse.com/i/piQHukj )
## OBJECTS

![image.png](https://s2.loli.net/2023/10/21/lxhNyV4QgnY867R.png)

equals 先调用也是调用 object. equals