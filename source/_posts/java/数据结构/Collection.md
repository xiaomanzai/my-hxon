---
title: collection
tags:
  - 数据结构
category: java ds
date: 2023-11-02 17:24:45
---
![collection](https://s2.loli.net/2023/11/05/d7XvW6iRON1DoyM.png)



## 迭代器

迭代器是集合专用遍历

iterator\<E> iterator () 返回迭代器对象 e 是集合中的元素类型

方法 
boolean hasNext () 判断当前位置有没有元素
E next () 获取当前元素并且移到下一个位置中

注意
1. 只能遍历一次不会复位
2. 每个元素只能使用一次 next 方法
3. 遍历时候不能用集合的方法进行删除或者增加
4. 只能用迭代器的方法进行删除 remove ()

#### lamada 增强 for 循环

for (E xx : collection\<E>)


### 可变参数

格式属性名... 名字
使用迭代器遍历

但是对于可变参数对于两个数组来说，就不太适用，因为可变参数第一个值会吃掉所有的值

如果还有其他的参数，可变参数要到最后一个




## collections


相比较
Arrays 是数组的工具类
集合的工具类


void addall (collection t , abs)

void shuffle (collection t) 打乱数据

swap, max/min, copy, 

#### 不可变集合

使用静态的 of 方法

static \<E> collection of (E... elements)

对于 set 和 list 的类的 of 是可变方法的参数
而对于 map 类的参数仅仅是20个，因此 map 类只能导入20个以下的参数

是因为只能有一个可变参数，因此 map 是不可能的