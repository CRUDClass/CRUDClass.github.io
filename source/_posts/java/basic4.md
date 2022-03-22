---
title: java基础四
categories: 
 - [Java,Java基础]
tags: 
 - Java基础
date: 2022-03-20 17:04:00
---

# Java 流程控制

### 一. Scanner 对象

- Scanner 可以实现人机交互 , java.util.Scanner 是Java 1.5 的新特性

- 基本用法

  ```java
  Scanner scanner = new Scanner(System.in);
  ```

- 使用 : 通过 Scanner 的 `next()` 和 `nextLine()` 方法获取输入的字符串 , 在读取前我们一般需要 使用 `hasNext()` 与 `hasNextLine()` 判断是否还有输入数据 . 

```java
// 使用
Scanner scanner = new Scanner(System.in);
System.out.println("请输入一串字符");
/// 判断是否输入 字符串
if(scanner.hasNext()){
    String str = scanner.next();
    System.out.println("输入的字符串: "+str);
}
// 结束
scannr.close();

```

```
// 使用
Scanner scanner = new Scanner(System.in);
System.out.println("请输入一串字符");
/// 判断是否输入 字符串
if(scanner.hasNextLine()){
    String str = scanner.nextLine();
    System.out.println("输入的字符串: "+str);
}
// 结束
scannr.close();
```

- `next()` , `nextLine()` 的区别
  - next()
    1. 读取到有效字符才可以结束输入 !
    2. 输入有效字符之前有空白 , next()  自动去除
    3. 只有输入有效字符才把后面的输入的空白座位分隔符或者结束符
    4. **`next()`** 不能获取有空格的字符串
  - nextLine()
    1. 以 `Enter` 为结束符 , `newxLine()` 获取`Enter` 之前的所有数据
    2. 可以有空格留空
- nextLine() 使用频率更高

### 二. 顺序结构

- Java 基本结构就是顺序结构 , 除非特别指示 , 否则就按照顺序一句一句执行 . 
- 顺序结构是最简单的算法结构 . 
- 语句与语句之间 , 框与框之间是按照从上到下的顺序进行的 , 他由若干个依次执行的处理步骤组成的 , 他是任何一个算法都离不开的一种基本算法结构 . 

### 三. 选择结构

1. `if` 选择结构

   ```java
   if(布尔表达式){
   // 表达式值为 true 走这里
   }
   
   // if 双选择结构
   if(布尔表达式){
   	// 表达式值为 true 走这里
   }else{
       // 表达式为 false 走这里
   }
   
   // if 多选择结构
   if(布尔表达式1){
   	// 表达式1值为 true 走这里
   }else if(布尔表达式2){
   	// 表达式值2为 true 走这里
   }else if(布尔表达式3){
   	// 表达式3值为 true 走这里
   }else{
       // 当以上表达式为 false 走这里
   }
   
   // 嵌套 if 结构 互相互不干扰
   if(布尔表达式3){
   	// 表达式3值为 true 走这里
       if(布尔表达式3){
   	// 表达式3值为 true 走这里
   }else{
       // 当以上表达式为 false 走这里
   }
   }else{
       // 当以上表达式为 false 走这里
   }
   
   ```

2. `switch` 多选择结构 

   ```java
   switch(expression){ // expression 可以为byte,short,int,char,String(jdk 7 之后)
       //可以添加 任意数量的 case 语句 value必须为字符串常量或字面量
       case value :　
           // 可以添加相关逻辑
           break; // break 可有可无 无break继续走下面的case(case穿透) 有break 终止 
       case value :　
           break;
       case value :　
           break;
       default : // 可有可无 有默认执行
           break;
   }
   // 如果 expression 类型为String 通过 hashCode() 判断
   ```

###  四. 循环结构

1. `while` 循环

   1. 
      
      ```java
      while(布尔表达式){ // 表达式为 true 时 就会循环执行 
          // 循环体
      }
      ```
      
      
      
   2. 大多数情况下会让表达式失效 值为 `false` 停止执行

   3. 循环条件为 `true` 会造成 一直循环死循环, 业务逻辑中避免出现死循环,死循环会导致程序崩溃或降低性能

2. `do` ... `while` 循环

   1. 
      
      ```java
      do{
          // 循环体
      }while(布尔表达式);
      ```
      
      
      
   2.  表达式不满足时也至少循环执行一次

   3. `while` 先判断后执行 `do` ... `while` 先执行一次在判断

3. `for` 循环

   1. 
      
      ```java
      for(定义初始循环控制变量并赋值;布尔表达式;循环控制变量变更){
          // 循环体
      }
      ```
      
      
      
   2. `for` 循环的两种方式
   
      ```java
      String[] x = ["a","b","c","d"];
      // 普通 for 循环
      for(int i = x.length-1 ; i >= 0 ;i--){
          System.out.println(x[i]);
      }
      // 增强 for 循环
      for(String i : x){
          System.out.println(i);
      }
      ```
   
      
   
   3. `for` 循环 更灵活,更高效

### 五. `break` 和`continue`

1. **break**
   - `break`控制循环的流程 .
   - `break`用于强行退出循环 , 不再进行剩下的循环 . 
   - `break`语句也在`switch`语句中使用 . 
2. **continue**
   - `continue`用于终止某次循环 . 
   - 结束本次循环 , 不再进行执行循环体中尚未执行的语句 , 进行下一次循环 . 

### 六. `goto`关键字

1. `goto` 是Java的一个保留字 , 但并未在语言中得到正式使用 ; Java 中没有goto

2. `标签`: 是指后面跟一个冒号的标识符 , 例如 : label:

   ```java
   // 不建议使用	
   outer:for(int i = 0 ; i < 500 ; i++){
       for(int j = 2 ; j < i/2 ; j++){
           if(i % j == 0){
               continue outer;
           }
       }
   }
   ```

   

