---
layout:     post
title:      "JAVA语言错题本"
subtitle:   "不适合人类阅读，非常水的自我笔记"
date:       2018-12-16
author:     "ABU"
header-img: "img/post-bg-unix-linux.jpg"
catalog: true
tags:
    - JAVA
    - Linux
---

```
double x=(double)9/5,x的值为：1.8

```
```
执行完下面程序片断之后，下面_____B__结论是正确的。
    int a, b, c;
    a=1;
    b=2;
    c=(a+b>3 ? a++:++b);
(A)  a的值是2，b的值是3           (B) a的值是1，b的值是3
(C)  a的值是1，b的值是2           (D) c的值是false
```
```
import java.util.Scanner; 
class Triangle{
	public static double areaOfTriangle(double a, double b, double c) {		// a行
		double s=(a+b+c)/2.0;
		return Math.sqrt(s*(s-a)*(s-b)*(s-c));
	}
	public static void main(String [] args)	{
		int x,y,z;   									                      // b行
		double s;
		Scanner reader = new Scanner(System.in);
		System.out.println("请输入三角形的三边长");
		x = reader.nextInt();
		y = reader.nextInt();
		z = reader.nextInt();
		s= areaOfTriangle(x,y,z);										
		System.out.println("三角形面积为："+s); 
	}
}
答案：6.0
```
```
把对象实例化可以生成多个对象，使用____new__运算符为对象分配内存空间。
```
```
( A )我们使用的UML 图是一个被分成个三部分矩形框，
最上面的部分存放. _______; 中间部分存放 _______; 底部存放 _______.
A、	类名; 域; 方法    B、	类名; 对象名; 方法   C、	对象名; 域; 方法

```
```
写出下列程序的输出结果
public class TestA{
public void printArray(int[] arr)   {
for(int i=0;i<arr.length;i++)
System.out.print(arr[i]+",");
System.out.println("\n");
}
public void changeValue(int value) {
value*=2;
}
public void changeValue(int[] arr) {
for(int i=0;i<arr.length;i++)
arr[i]*=2;
}
}
public class TestB{
public static void main (String[] args) {
int[] arr={1,2,3,4,5};
TestA a=new TestA();
a.changeValue(arr[0]);
a.printArray(arr);
a.changeValue(arr);
a.printArray(arr);
}
}
答案：
 1,2,3,4,5,
 2,4,6,8,10
```
```
( B )如果object1 和object2是同一个类的对象, 为了使 object2是object1的副本，应该_______。
A、	将object1 赋值给object2, 即object2 = object1;
B、	写一个复制方法将object1 中域的值一个一个赋值给object2中对应的域
C、	使用Java语言中的copy方法
D、	使用缺省的构造方法，用object1 的域来创建object2 
```
```
fanya-4-28下面的类和接口定义正确的是：_____________
A、
public class A { 
    private int x; 
    public getx() {  
        return x;  }
 } 

B、
public abstract class A{
    private int x; 
    public abstract int getx(); 
    public int amethod() {
        return 0;  
    } 
} 

C、
public class A { 
    private int x; 
    public abstract int getx(); 
} 

D、
public interface Interfacea { 
    private int x; 
    public int getx() {
        return x;  
    } 
}
答案：A不对
```
```
fanya-4-50下列哪种说法是正确的（）
A、实例方法可直接调用超类的实例方法
B、实例方法可直接调用超类的类方法
C、实例方法可直接调用其他类的实例方法
D、实例方法可直接调用本类的类方法
我的答案：B error
```
```
4．	在一个合法的Java源程序文件中定义了3个类，则其中属性为public的类可能有__A___个。
 (A)  1			   (B)  2        (C)  3		 (D)  A、B、C都有可能

```
```
下面程序的输出是____AB.B_____。

class J_StringBuffer{

    public static void main(String args[]){
        StringBuffer a = new String(“A”);
        StringBuffer b = new String(“B”);
        mb_operate(a,b);
        System.out.println(a + “.” + b );
    }

    static void mb_operate(StringBuffer x, StringBuffer y){
        x.append(y);
        y=new StringBuffer(“AB”);
    }
}
（3.0分）
```
```
下面程序输出（    ）。
public class Test{
public static void main(String[] args){
 Count myCount = new Count();
int times = 0;
for(int i=0;i<100;i++)
increment(myCount , times);
System.out.println("count is" + myCount.count);
System.out.println("time is"+ times);
}
public static void increment(Count c , int times){
c.count++;
times++;
}
}
class Count{
public int count;
Count(int c){
count =c;
}
Count(){
count =1;
}
}
答案：
count is 101
time is 0
```
```
读程序，程序输出结果是（   5  ）。

class SimpleValue{

public static void change(int x)    {

x = 3;

}

public static void main(String [] args)    {

int x = 5;

change(x);

System.out.println(x);

}

}
（3.0分）
```
```
认真阅读下面的程序：
class  TestApp{
  public static void main(String[] args){
         for(int i=0;i<5;i++)
              System.out.print(i+1);
         System.out.println(i);
    }
}
上述程序运行后的结果是（     D     ）
（3.0分）
A 123456
B 123455
C 123450
D 编译错误
```
