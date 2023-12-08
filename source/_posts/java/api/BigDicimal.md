---
title: BigDicimal
tags:
  - java
category: java api
date: 2023-11-02 17:24:45
---



## 构造方法

1. double 数
2. 字符串

## 方法


``` java
 BigDecimal add (BigDecimal) 
 BigDecimal subtract (BigDecimal)
 BigDecimal multiply (BigDecimal)
 BigDecimal divide (BigDecimal)
 BigDecimal divide (BigDecimal, 精确位数)
 ps：divide(BigDecimal,2,BigDecimal.ROUND_HALF_UP) 四舍五入，保留两位
 ```

## 底层


把 double 变成一个字符串来存放 acill 码在 byte 数组当中
