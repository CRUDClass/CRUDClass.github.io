---
title: java基础六
categories: 
 - [Java,Java基础]
tags: 
 - Java基础
date: 2022-03-20 17:06:00
---

## 数组

### 一. 数组的概述

####　数组的定义

数组是相同类型数据的有序集合 . 是相同类型的若干数据 , 按照一定的先后次序排列组合而成 . 其中每一个数据称作一个数组元素 , 每个数组元素可以通过一个下标来访问它 .

#### 数组的四个基本特点

- 其长度是确定的 . 数组一旦被创建 , 他的大小就是不可以改变的 .
- 其元素必须是想同类型 , 不允许出现混合类型 .
- 数组中元素可以是任意数据类型 , 包括基本数据类型和引用类型
- 数组变量属引用类型 , 数组也可以看成是对象 , 数组中的每个元素相当于该对象成员的变量 . 数组本身就是对象 , java中对象实在堆中 , 因此数组无论保存原始类型还是其他对像类型 , **数组对象本身是在堆中 **. 

### 二. 数组的声明和创建

1. 首先必须声明数组变量 , 才能在程序中使用数组 .

```java
dataType [] array;
dataType array[];
```

2. java语言使用 `new` 操作符来创建数组 .

```java
dataType[] array = new dataType[arraySize];
```

3. 数组元素通过索引访问 , 数组索引从 `0` 开始
4. 数组长度 `arrays.length`

### 三. 数组使用

#### 声明一个数组元素

```java
// 声明一个元素2
int num[];
int[] num;

```

#### 创建一个数组

```java
num = new int[10]; // 创建一个空间为10 的数组
```

#### 赋值

```java
num[0] = 1;// 给数组赋值
```

####  创建并赋值

```java
int[] i = {1,2,3,4,5,6,7,8,9,0};
```

#### 数组的默认初始化

数组是引用类型 , 它的元素相当于类的实例变量 , 因此数组一经分配空间 , 其中每个元素也被按照实例变量同样的方式被隐式初始化 . 

#### for 循环

```java
int[] arrays = {1,2,3,4,5,6};
for(int i = 0 ; int < arrays.length ; i++){
    System.out.println(arrays[i]);
}
for(int array : arrays){
    System.out.println(array);
}
```

#### 数组做方法入参

```java
int[] arrays = {1,2,3,4,5,6};
printArrays(arrays);
public void printArrays(int[] arrays){
    for(int array : arrays){
    	System.out.println(array);
	}
}
```

#### 数组做返回值

```java
int[] arrays = new int[10];
arrays = valueArrays(arrays);
public int[] valueArrays(int[] array){
    int[] arrays = new int[array.length];
    for(int i = 0 ; int < arrays.length ; i++){
    	arrays[i] = i;
	}
    return arrays;
}
```

### 四. 多维数组

多维数组可以看成是数组的数组，比如二维数组就是一个特殊的一维数组，其每一个元素都是一个一维数组

```java
// 例
String[][] str = new String[3][4];
```

#### 多维数组的动态初始化（以二维数组为例）

```java
// 格式 : type[][] typeName = new type[typeLength1][typeLength2];
// type 可以为基本数据类型和复合数据类型，typeLength1 和 typeLength2 必须为正整数，typeLength1 为行数，typeLength2 为列数
// 例
int[][] a = new int[2][3];
```

#### 多维数组的引用（以二维数组为例)

```java
// 对二维数组中的每个元素，引用方式为 arrayName[index1][index2]
num[1][0];
```

### 五. Arrays 类

`java.util.Arrays` 类能方便地操作数组，它提供的所有方法都是静态的。

- 给数组赋值：通过 fill 方法。
- 对数组排序：通过 sort 方法,按升序。
- 比较数组：通过 equals 方法比较数组中元素值是否相等。
- 查找数组元素：通过 binarySearch 方法能对排序好的数组进行二分查找法操作。

| 序号 | 方法和说明                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | **public static int binarySearch(Object[] a, Object key)** 用二分查找算法在给定数组中搜索给定值的对象(Byte,Int,double等)。数组在调用前必须排序好的。如果查找值包含在数组中，则返回搜索键的索引；否则返回 (-(*插入点*) - 1)。 |
| 2    | **public static boolean equals(long[] a, long[] a2)** 如果两个指定的 long 型数组彼此*相等*，则返回 true。如果两个数组包含相同数量的元素，并且两个数组中的所有相应元素对都是相等的，则认为这两个数组是相等的。换句话说，如果两个数组以相同顺序包含相同的元素，则两个数组是相等的。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |
| 3    | **public static void fill(int[] a, int val)** 将指定的 int 值分配给指定 int 型数组指定范围中的每个元素。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |
| 4    | **public static void sort(Object[] a)** 对指定对象数组根据其元素的自然顺序进行升序排列。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |

### 六. 稀疏数组

当一个数组中大部分元素为**0**时 , 或者为统一数值时 , 可以通过稀疏数组来保存数据 . 

#### 处理方式

- 记录数组一共有几行几列 , 有多少个不同值 .
- 把具有不同值的元素和行列及值记录在一个小规模的数组中 , 从而缩小程序的规模 .

```java
 public static void main(String[] args) {

        /**
         * 初始化二维数组
         * <p>
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 1 0 0 0 0 0 0 0 0
         *     0 0 0 0 2 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         * </p>
         */
        //初始化原数组
        int[][] array = new int[11][11];
        array[1][2] = 1;
        array[2][4] = 2;
        for(int[] row : array){
            for(int item : row){
                System.out.printf("%d\t",item);
            }
        }

        System.out.println("---------> 二维数组转稀疏数组");

        /**
         * 稀疏数组
         * <p>
         *     11 11 2
         *     1  2  1
         *     2  4  2
         * </p>
         */
        //得到非0数据数
        int sum = 0;
        for (int i = 0;i<11;i++){
            for(int j = 0;j<11;j++){
                if(array[i][j] != 0){
                    sum++;
                }
            }
        }
        //创建稀疏数组
        int[][] sparseArray = new int[sum+1][3];
        //给稀疏数组赋值
        sparseArray[0][0] = 11;
        sparseArray[0][1] = 11;
        sparseArray[0][2] = sum;
        //将非0的数放入稀疏数组
        //count：标识第几个非0数
        int count = 0;
        for (int i = 0;i<11;i++){
            for(int j = 0;j<11;j++){
                if(array[i][j] != 0){
                    count++;
                    sparseArray[count][0] = i;
                    sparseArray[count][1] = j;
                    sparseArray[count][2] = array[i][j];
                }
            }
        }
        //遍历稀疏数组
        for(int i = 0;i<sparseArray.length;i++){
            System.out.printf("%d%d%d\t",sparseArray[i][0],sparseArray[i][1],sparseArray[i][2]);
        }

        System.out.println("----------->稀疏数组转回原始数组");

        /**
         * 恢复的二维数组
         * <p>
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 1 0 0 0 0 0 0 0 0
         *     0 0 0 0 2 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         *     0 0 0 0 0 0 0 0 0 0 0
         * </p>
         */

        int[][] oldArray = new int[sparseArray[0][0]][sparseArray[0][1]];
        //将原来非0的数填充回去
        for(int i = 1;i<=count;i++){
          oldArray[sparseArray[i][0]][sparseArray[i][1]] = sparseArray[i][2];
        }
        //遍历刚转回的原始数组
        for(int[] row : oldArray){
            for(int item : row){
                System.out.printf("%d\t",item);
            }
        }
    }
```

