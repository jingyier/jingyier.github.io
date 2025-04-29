---
title: java学习
date: 2025-04-29 19:22:38
tags: [学习]
---
## 异常处理
### 一、异常语句块处理

#### 1.自己异常处理
try cathc语句
#### 2.单个异常处理
```
try{
     //防止肯出现异常的代码
}catch(异常类型 异常名称){
     //放置处理异常的代码
     }finally{
     //释放资源
     }
```
```
ublic class Exception {

    public static void main(String[] args) {
        System.out.println("第一段码");
        int i=5;
        try {
            System.out.println(i/0);
        }catch (ArithmeticException e){
            System.out.println("除数为0");
        }


        System.out.println("第二段码");
    }
}
```
catch捕获的异常要和实际抛出的异常要么一致，要么有继承关系

#### 3.多个异常处理
- try 块中有多行代码，都有可能出现异常信息，程序执行的时候是从上往下执行的，当碰到异常情况的时候就会跳出try块，
从而剩下的就不会执行了
- printStackTrace()方法可以给出详细的异常信息

### 二、将异常抛出
```
public class Exception {

    public static void main(String[] args) {

        try{
            calc();
        }catch (ArithmeticException e){
            e.printStackTrace();
        }

        System.out.println("第一段码");


    }

    public static int calc() throws ArithmeticException{
        int a = 10;
        int b = 0;
        int result = a / b;
        return result;
    }
}
```
throws的使用格式
```
[修饰符]返回值类型 方法名(参数列表)[throws 异常1,异常2...]{   }

```
1. 注意：
- 如果一个方法声明的是编译时异常，则在调用这个方法之处必须处置这个异常（谁调用，谁处理）
- 异常子类可以抛给父类，父类不能抛给子类
2. throws作用：在定义一个方法的时候可以使用throws关键字声明，使用throws关键字声明的方法表示此方法不处理异常，而交给方法的调用者进行处理

### 三、throw关键字

