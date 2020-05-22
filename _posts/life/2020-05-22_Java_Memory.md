---
layout: post
title: java内存管理
category: java技术
tags: essay
keywords: java,内存管理,内存回收
description:
---

# java堆内存与垃圾回收（garbage collection）

## 栈内存
主要保存基本数据类型变量的值（short int long float double char boolean byte）、对象的引用（对象保存在堆中）。
### 特点：
- 栈内存中所保存的变量有两个特点，生存期确定和占用内存大小确定。（生存期结束后会立马释放所占用的内存空间）
- 栈内存的存取速度非常快，仅次于寄存器。
- 栈内存中保存的变量是共享的。（int a=3,b=3  a==b返回true）

## 堆内存
主要保存通过new关键字生成的对象，以及数组。
### 特点：
- 堆内存中保存的变量大小不固定，生存期也不固定。（由JVM GC garbage collector进行垃圾回收）
- 堆内存的存取速度不如栈内存。

## 常量池
主要保存编译时已经确定，并被保存在已编译的.class文件中的一些数据，除了包含在代码中的基本数据类型变量还包含对象的常量值（final）。
### 特点：
- 常量池中的变量不是保存在堆内存中，则是保存在方法区中。
- 常量池中的变量是共享的


# 垃圾回收机制（GC,garbage collection）
由于栈内存中保存的变量的生存期和大小都是确定的，因此，变量生存期到了之后，会自动释放掉。
一般我们讲到的GC或者Java 垃圾回收机制都是针对于堆内存而言的，只有堆内存中的变量生存期和大小是不确定的，需要JVM 进行垃圾回收。

## 堆内存保存变量的区域按照变量的状态可以划分为三个区域：
- 
![](https://github.com/thimberg/thimberg.github.io/blob/master/_posts/life/javaMemory1.PNG)
- ｌｌ
![](https://github.com/thimberg/thimberg.github.io/blob/master/_posts/life/20150330212335.png)

- Java 的多线程编程
- Elasticsearch 的使用和优化
- 万亿级别数据的处理和优化

这几个方面逐渐也有了一些心得和沉淀，准备找个时间总结一下。

## 生活

2018 比较开心的一点就是 H1B 总算抽中，虽然得多交 10% 的税，但是至少可以不用担心自己的身份问题了。但是也因为 H1B 的申请，我从 4 月到 10 月之间都没有办法离开美国，所以之前计划的日本和台湾行都搁置了，只有 10 月回国一趟还算适当放松了一下。




