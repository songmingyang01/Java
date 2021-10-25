# Java
Java作业实验一

## 一、业务要求
&emsp;&emsp;求三维空间中两个给定点的距离。
## 二、解题思路
1. 首先，需要设置一个类（Port），是每一个点的坐标。建立三个成员变量（x,y,z）来存入三个坐标量。并设置构造函数，初始化三个坐标数值。
2. 然后，设置方法（jisuan），根据公式，计算两个点之间的距离。并且使其输出运算结果。
3. 设置主函数，创建两个Port对象，并使用构造函数赋值。然后调用计算公式，计算并显示结果。
4. 在运行过程中，我认为只显示运行结果不够直观，于是又添加了一个函数（show），用来显示点坐标。
## 三、关键代码
1. 设置成员变量，以及构造函数。
```java
    double x;
    double y;
    double z;
    public Port(double a,double b,double c){
        x = a;
        y = b;
        z = c;
    }
```
2. jisuan方法，根据公式计算。该方法通过引入另外一个对象作为变量的方式，在两个对象之间做运算。分别求出两个坐标的x,y,z之差，平方求和，开根号。
```java
    public double jisuan(Port aa){
        double h;
        h = Math.sqrt((aa.x - this.x)*(aa.x - this.x)+(aa.y - this.y)*(aa.y - this.y)+(aa.z - this.z)*(aa.z - this.z));
        System.out.println("结果为"+h);
        return h;
    }
```
3. 设置主函数，初始化两个对象的成员变量，然后调用函数，计算求值，显示。
```java
    public static void main(String[] args){
        Port port1 = new Port(2,3,4);
        Port port2 = new Port(7,8,5);
        port1.show();
        port2.show();
        port1.jisuan(port2);
```
