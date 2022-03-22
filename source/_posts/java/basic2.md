---
title: java基础二
categories: 
 - [Java,Java基础]
tags: 
 - Java基础
date: 2022-03-20 17:02:00
---

# JAVA基础语法

1. 注释

1. 单行注释	`// 文本`
2. 多行注释    `/* 文本 */`
3. 文本注释    `/** 文本 */`
4. 有趣的代码注释 哈哈


```java
/***
 *             ,%%%%%%%%,
 *           ,%%/\%%%%/\%%
 *          ,%%%\c "" J/%%%
 * %.       %%%%/ o  o \%%%
 * `%%.     %%%%    _  |%%%
 *  `%%     `%%%%(__Y__)%%'
 *  //       ;%%%%`\-/%%%'
 * ((       /  `%%%%%%%'
 *  \\    .'          |
 *   \\  /       \  | |
 *    \\/         ) | |
 *     \         /_ | |__
 *     (___________))))))) 攻城湿
 *
 *        _       _
 * __   _(_)_   _(_) __ _ _ __
 * \ \ / / \ \ / / |/ _` |'_ \
 *  \ V /| |\ V /| | (_| | | | |
 *   \_/ |_| \_/ |_|\__,_|_| |_|
 */

```

#####  2. 标识符

- 关键字 ↓常用关键字

  <table class="table-view log-set-param"><tbody><tr><td><strong>关键字</strong></td><td><strong>含义</strong></td></tr><tr><td>abstract</td><td>表明类或者成员方法具有抽象属性</td></tr><tr><td>assert</td><td>断言，用来进行程序调试</td></tr><tr><td>boolean</td><td>基本数据类型之一，布尔类型</td></tr><tr><td>break</td><td>提前跳出一个块</td></tr><tr><td>byte</td><td>基本数据类型之一，字节类型</td></tr><tr><td>case</td><td>用在switch语句之中，表示其中的一个分支</td></tr><tr><td>catch</td><td>用在异常处理中，用来捕捉异常</td></tr><tr><td>char</td><td>基本数据类型之一，字符类型</td></tr><tr><td>class</td><td>声明一个类</td></tr><tr><td>const</td><td>保留关键字，没有具体含义</td></tr><tr><td>continue</td><td>回到一个块的开始处</td></tr><tr><td>default</td><td>默认，例如，用在switch语句中，表明一个默认的分支</td></tr><tr><td>do</td><td>用在do-while循环结构中</td></tr><tr><td>double</td><td>基本数据类型之一，双精度浮点数类型</td></tr><tr><td>else</td><td>用在条件语句中，表明当条件不成立时的分支</td></tr><tr><td>enum</td><td>枚举</td></tr><tr><td>extends</td><td>表明一个类型是另一个类型的子类型，这里常见的类型有类和接口</td></tr><tr><td>final</td><td>用来说明最终属性，表明一个类不能派生出子类，或者成员方法不能被覆盖，或者成员域的值不能被改变，用来定义常量</td></tr><tr><td>finally</td><td>用于处理异常情况，用来声明一个基本肯定会被执行到的语句块</td></tr><tr><td>float</td><td>基本数据类型之一，单精度浮点数类型</td></tr><tr><td>for</td><td>一种循环结构的引导词</td></tr><tr><td>goto</td><td>保留关键字，没有具体含义</td></tr><tr><td>if</td><td>条件语句的引导词</td></tr><tr><td>implements</td><td>表明一个类实现了给定的接口</td></tr><tr><td>import</td><td>表明要访问指定的类或包</td></tr><tr><td>instanceof</td><td>用来测试一个对象是否是指定类型的实例对象</td></tr><tr><td>int</td><td>基本数据类型之一，整数类型</td></tr><tr><td>interface</td><td>接口</td></tr><tr><td>long</td><td>基本数据类型之一，长整数类型</td></tr><tr><td>native</td><td>用来声明一个方法是由与计算机相关的语言（如C/C++/FORTRAN语言）实现的</td></tr><tr><td>new</td><td>用来创建新实例对象</td></tr><tr><td>package</td><td>包</td></tr><tr><td>private</td><td>一种访问控制方式：私用模式</td></tr><tr><td>protected</td><td>一种访问控制方式：保护模式</td></tr><tr><td>public</td><td>一种访问控制方式：共用模式</td></tr><tr><td>return</td><td>从成员方法中返回数据</td></tr><tr><td>short</td><td>基本数据类型之一,短整数类型</td></tr><tr><td>static</td><td>表明具有静态属性</td></tr><tr><td>strictfp</td><td>用来声明FP_strict（单精度或双精度浮点数）表达式遵循<a href="https://baike.baidu.com/item/IEEE%20754"><u><span style="color:#0066cc;">IEEE 754</span></u></a>算术规范<sup class="sup--normal"><span style="font-size:12px;"> [1]</span></sup><a class="sup-anchor">&nbsp;</a></td></tr><tr><td>super</td><td>表明当前对象的父类型的引用或者父类型的构造方法</td></tr><tr><td>switch</td><td>分支语句结构的引导词</td></tr><tr><td>synchronized</td><td>表明一段代码需要同步执行</td></tr><tr><td>this</td><td>指向当前实例对象的引用</td></tr><tr><td>throw</td><td>抛出一个异常</td></tr><tr><td>throws</td><td>声明在当前定义的成员方法中所有需要抛出的异常</td></tr><tr><td>transient</td><td>声明不用序列化的成员域</td></tr><tr><td>try</td><td>尝试一个可能抛出异常的程序块</td></tr><tr><td>void</td><td>声明当前成员方法没有返回值</td></tr><tr><td>volatile</td><td>表明两个或者多个变量必须同步地发生变化</td></tr><tr><td rowspan="1" colspan="1">while</td><td rowspan="1" colspan="1">用在循环结构中</td></tr></tbody></table>

- ***Java 所有组成部分都需要名字. 类名,变量名及方法名都被称为标识符.***

- ***所有标识符都应该以字母( A-Z 或者 a-z ) , 美元符号( $ ) , 或者下划线( _ ) 开始*** 
- ***首字母之后可以是字母( A-Z 或者 a-z ) , 美元符号( $ ) , 或者下划线( _ ) 和数字 随意组合***
- ***<font color = "red">不能使用关键字作为变量名或方法名 .</font>***
- ***标识符是<font color="red">大小写敏感</font>的 .***
- ~~***可以使用中文命名,但是一般不建议这样使用,也不建议使用拼音***~~