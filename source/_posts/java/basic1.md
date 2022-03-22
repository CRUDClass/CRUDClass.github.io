---
title: java基础一
categories: 
 - [Java,Java基础]
tags: 
 - Java基础
date: 2022-03-20 17:01:00
---

### java的特性和优势

1. 简单性
2. 面向对象
3. 可移植性
4. 高性能
5. 分布式
6. 动态性
7. 多线程
8. 安全性
9. 健壮性
10. 使用的人多

### JDK,JRE,JVM的关系

1. JDK  : Java Development Kit java 开发者工具包含JRE和JVM

2. JRE  : Java Runtime Environment JAVA 运行环境包含JVM

3. JVM : Java Virtual Machine JAVA 虚拟机

### 删除JDK( windows 环境)

1. 删除  java ~~***环境变量***~~ ( JAVA_HOME , Path 下 JAVA相关)
2. 删除 java 目录 或 卸载 java
3. java -version 测试

### 安装JDK ( windows环境)

1. [根据不同系统下载对应版本下载JDK8](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html) 

2. 双击安装 JDK

3. 记住安装目录

4. 配置环境变量

   1. 此电脑->属性->高级系统设置->环境变量
   2. 系统变量添加 JAVA_HOME 
      - 变量名: JAVA_HOME 变量值 : E:\Tools\JDK-8
   3. 用户变量 在Path 下添加 
      - %JAVA_HOME%\bin
      - %JAVA_HOME%\jre\bin

   4. 打开 cmd java -version 测试 JDK是否安装成功

### Hello World!

1. 新建文件 HelloWorld.java 首字母大写

```java
public class HelloWorld{
    public static void main(String[] ages){
        System.out.print("Hello World!");
    }
}
```

2. 在当前文件夹目录下运行 **javac HelloWorld.java** 在当前文件夹编译生成 **HelloWorld.class**
3. 在当前文件夹目录下运行 **java HelloWorld.class** 控制台打印 ***Hello World!***

### JAVA 程序运行机制

java 及时解释型也是编译型语言

**运行机制**

原程序 `*.java`文件 通过 --> Java编译器 转换为 --> 字节码`*.claa` 文件 --> 放入虚拟机的 类装载器中 --> 字节码校验器 --> 解释器 --> 操作系统平台

先编译 --> 在解释

### 安装运行软件

idea

### 来源

- 哔哩哔哩 [遇见狂神说](https://space.bilibili.com/95256449/?spm_id_from=333.999.0.0)
