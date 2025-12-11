- 按照每周的要求来分块
- 无论是自学还是教学内容，全部放在一个框架里面


[[#考试]]




| Date                    | Module                                                                                                 | Learning activities                                                                                                                                                                                                                   | Assessment                                   |     |
| ----------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | --- |
| [[#Week 1]]             | Module 1: Introduction to programming  <br>  <br>Module 2: Introduction to object-oriented programming | Discussion 1: Introduce yourself  <br>  <br>Activity: Lab 1 - Introduction to programming  <br>  <br>Activity: Module 1 Self Assessment Quiz   <br>  <br>Activity: Lab 2 - OOP  <br>  <br>Activity: Module 2 OOP Self Assessment Quiz |                                              |     |
| [[#Week 2]]             | Module 3: Control flow                                                                                 | Activity: Lab 3 - Control flow  <br>  <br>Activity: Module 3 Control flow Self Assessment Quiz                                                                                                                                        |                                              |     |
| [[#Week 3]]             | Module 4: [[#Arrays and classes  ]]<br>  <br>Module 5: [[#Inheritance]]                                | Activity: Lab 4 - Arrays and classes  <br>  <br>Activity: Module 4 Arrays and classes Self Assessment Quiz  <br>  <br>Activity: Lab 5 - Inheritance  <br>  <br>Activity: Module 5 Inheritance Self Assessment Quiz                    | **[[#Test 1]]**<br>  <br>**Interview 1**     |     |
| [[#Week 4]]             | Module 6: UML  <br>  <br>Module 7: Exception handling                                                  | Activity: Lab 6 - UML  <br>  <br>Activity: Module 6 UML Self Assessment Quiz  <br>  <br>Activity: Lab 7 - Exception handling  <br>  <br>Activity: Module 7 Exception handling Self Assessment Quiz                                    |                                              |     |
| [[#Week 5]]             | Module 8: I/O  <br>  <br>Module 9: Collections                                                         | Activity: Lab 8 - I/O  <br>  <br>Activity: Module 8 I/O Self Assessment Quiz  <br>  <br>Activity: [[#Lab 9 - Collections  ]]<br>  <br>Activity: Module 9 Collections Self Assessment Quiz                                             | Test 2                                       |     |
| [[#Week 6]]             | Module 10: More on collections  <br>  <br>Module 11: Recursion                                         | Activity: Lab 10 - More on collections  <br>  <br>Activity: Module 10 More on collections Self Assessment Quiz  <br>  <br>Activity: Labs 11 - Recursion  <br>  <br>Activity: Module 11 Recursion Self Assessment Quiz                 |                                              |     |
| [[#Mid-semester break]] |                                                                                                        |                                                                                                                                                                                                                                       |                                              |     |
| [[#Week 7]]             | Module 12: Introduction to testing                                                                     | Activity: Labs 12 - Introduction to testing  <br>  <br>Activity: Module 12 Introduction to testing Self Assessment Quiz                                                                                                               | Test 3                                       |     |
| [[#Week 8]]             | Module 13 & 14: Swing                                                                                  | Activity: Lab 13 & 14 - Swing  <br>  <br>Activity: Module 13 & 14 Swing Self Assessment Quiz                                                                                                                                          |                                              |     |
| [[#Week 9]]             | Module 15 & 16: Design patterns                                                                        | Activity: Lab 15 & 16 - Design patterns  <br>  <br>Activity: Module 15 & 16 Self Assessment Quiz                                                                                                                                      |                                              |     |
| [[#Week 10]]            | Module 17: Refactoring                                                                                 | Activity: Lab 17 - Refactoring                                                                                                                                                                                                        | Test 4  <br>  <br>Interview 2                |     |
| [[#Week 11]]            | Introduction to Final Project                                                                          |                                                                                                                                                                                                                                       |                                              |     |
| Week 12                 |                                                                                                        |                                                                                                                                                                                                                                       |                                              |     |
| [[#Week 13]]            |                                                                                                        |                                                                                                                                                                                                                                       | Final project code, presentation, and report | #   |


---------------

#  week 1



## 基本数据类型
##### 内置数据类型

Java语言提供了八种基本类型。六种数字类型（四个整数型，两个浮点型），一种字符类型，还有一种布尔型。

**byte：**

- byte 数据类型是8位、有符号的，以二进制补码表示的整数；
- 最小值是 -128（-2^7）；
- 最大值是 127（2^7-1）；
- 默认值是 0；
- byte 类型用在大型数组中节约空间，主要代替整数，因为 byte 变量占用的空间只有 int 类型的四分之一；
- 例子：byte a = 100，byte b = -50。

**short：**

- short 数据类型是 16 位、有符号的以二进制补码表示的整数
- 最小值是 -32768（-2^15）；
- 最大值是 32767（2^15 - 1）；
- Short 数据类型也可以像 byte 那样节省空间。一个short变量是int型变量所占空间的二分之一；
- 默认值是 0；
- 例子：short s = 1000，short r = -20000。

**int：**

- int 数据类型是32位、有符号的以二进制补码表示的整数；
- 最小值是 -2,147,483,648（-2^31）；
- 最大值是 2,147,483,647（2^31 - 1）；
- 一般地整型变量默认为 int 类型；
- 默认值是 0 ；
- 例子：int a = 100000, int b = -200000。

**long：**

- long 数据类型是 64 位、有符号的以二进制补码表示的整数；
- 最小值是 -9,223,372,036,854,775,808（-2^63）；
- 最大值是 9,223,372,036,854,775,807（2^63 -1）；
- 这种类型主要使用在需要比较大整数的系统上；
- 默认值是 0L；
- 例子： long a = 100000L，long b = -200000L。  
    "L"理论上不分大小写，但是若写成"l"容易与数字"1"混淆，不容易分辩。所以最好大写。

**float：**

- float 数据类型是单精度、32位、符合IEEE 754标准的浮点数；
- float 在储存大型浮点数组的时候可节省内存空间；
- 默认值是 0.0f；
- 浮点数不能用来表示精确的值，如货币；
- 例子：float f1 = 234.5f。

**double：**

- double 数据类型是双精度、64 位、符合 IEEE 754 标准的浮点数；
- 浮点数的默认类型为 double 类型；
- double类型同样不能表示精确的值，如货币；
- 默认值是 0.0d；

**boolean：**

- boolean数据类型表示一位的信息；
- 只有两个取值：true 和 false；
- 这种类型只作为一种标志来记录 true/false 情况；
- 默认值是 false；
- 例子：boolean one = true。

**char：**

- char 类型是一个单一的 16 位 Unicode 字符；
- 最小值是 \u0000（十进制等效值为 0）；
- 最大值是 \uffff（即为 65535）；
- char 数据类型可以储存任何字符；
- 例子：char letter = 'A';。


### 自动类型转换

**整型、实型（常量）、字符型数据可以混合运算。运算中，不同类型的数据先转化为同一类型，然后进行运算。**

转换从低级到高级。

`低  ------------------------------------>  高`
`byte,short,char—> int —> long—> float —> double `


> **Java 的 variables（变量） 和基本类型（primitive types）到底是什么？**
> **为什么讲变量的时候，会提到 type（类型）？**



**Java 里面的两大类类型（types）**

✔ 1）基本类型（Primitive Types）

这是 Java 最底层、最基础的数据类型：

| **基本类型**    | **含义**       |
| ----------- | ------------ |
| byte        | 8位整数         |
| short       | 16位整数        |
| **int**     | 32位整数（最常用）   |
| long        | 64位整数        |
| **double**  | 小数（最常用）      |
| float       | 小数           |
| **boolean** | true / false |
| **char**    | 一个字符         |



这些是固定大小、速度快、存储在栈（stack）中的真实值。


✔ 2）引用类型（Reference Types）

比如：
	•	String
	•	你自己写的类：Employee、Dog
	•	数组
	•	ArrayList

这些不是直接放值，而是放引用（地址），实际对象在堆（heap）里。


## 变量类型

|**类型**|**在哪里声明？**|**生命周期**|**是否有默认值？**|**属于谁？**|
|---|---|---|---|---|
|**局部变量 local variable**|方法内部|方法执行结束后消失|❌ 没默认值|属于“代码块”|
|**实例变量 instance variable**|类中、方法外|对象活着就活着|✔ 有默认值|属于“对象”|
|**类变量 static variable**|类中用 static|程序运行期间一直在|✔ 有默认值|属于“类本身”|
|**参数变量 parameter**|方法小括号里|方法执行期间有效|❌ 没默认值（调用者必须传）|属于“方法”|

```java
public class RunoobTest {
    // 成员变量
    private int instanceVar;
    // 静态变量
    private static int staticVar;
    
    public void method(int paramVar) {
        // 局部变量
        int localVar = 10;
        
        // 使用变量
        instanceVar = localVar;
        staticVar = paramVar;
        
        System.out.println("成员变量: " + instanceVar);
        System.out.println("静态变量: " + staticVar);
        System.out.println("参数变量: " + paramVar);
        System.out.println("局部变量: " + localVar);
    }
    
    public static void main(String[] args) {
        RunoobTest v = new RunoobTest();
        v.method(20);
    }
}
```

> 定义了一个 RunoobTest 类，其中包含了一个成员变量 instanceVar 和一个静态变量 staticVar。
> method() 方法中定义了一个参数变量 paramVar 和一个局部变量 localVar。在方法内部，我们将局部变量的值赋给成员变量，将参数变量的值赋给静态变量，



方法参数变量的值传递方式有两种：**值传递**和**引用传递**。

- **值传递：** 在方法调用时，传递的是实际参数的值的副本。当参数变量被赋予新的值时，只会修改副本的值，不会影响原始值。Java 中的基本数据类型都采用值传递方式传递参数变量的值。
    
- **引用传递:** 在方法调用时，传递的是实际参数的引用（即内存地址）。当参数变量被赋予新的值时，会修改原始值的内容。Java 中的对象类型采用引用传递方式传递参数变量的值。


##### Java 局部变量（Local Variable）相关术语中英文对照

| **中文关键词** | **英文表达**                               | **解释说明**                    |
| --------- | -------------------------------------- | --------------------------- |
| 局部变量      | **local variable**                     | 声明在方法、构造器或代码块中的变量，只在该范围内有效  |
| 实例变量      | **instance variable**                  | 声明在类中、但不在方法中的变量（属于对象）       |
| 类变量       | **class variable / static variable**   | 使用 static 修饰的变量（属于类）        |
| 声明        | **declaration**                        | 创建变量的语句（如 int x;）           |
| 赋值        | **assignment**                         | 给变量设置值（如 x = 5;）            |
| 初始化       | **initialization**                     | 声明变量时赋初值（如 int x = 5;）      |
| 作用域       | **scope**                              | 变量在程序中可被访问的区域               |
| 生命周期      | **lifecycle / lifetime**               | 变量从创建到销毁的时间范围               |
| 方法        | **method**                             | Java 中可执行的函数块               |
| 构造方法      | **constructor**                        | 用于创建对象的特殊方法                 |
| 语句块       | **block / code block**                 | {} 包裹的代码区域                  |
| 编译器       | **compiler**                           | 将源代码翻译为字节码的程序               |
| 报错        | **compile-time error / runtime error** | 编译期或运行期错误                   |
| 栈内存       | **stack memory**                       | JVM 用于存储局部变量的内存区域           |
| 堆内存       | **heap memory**                        | JVM 用于存储对象的内存区域             |
| 垃圾回收      | **garbage collection (GC)**            | JVM 自动释放不再使用的对象或变量          |
| 命名冲突      | **naming conflict / name collision**   | 不同作用域中的变量同名导致混淆             |
| 可见性       | **visibility**                         | 哪些地方可以访问某个变量                |
| 参数        | **parameter / argument**               | 方法定义或调用时传入的值                |
| 返回值       | **return value**                       | 方法执行后返回的结果                  |
| 栈帧        | **stack frame**                        | JVM 为每个方法调用分配的内存区域          |
| 生效范围      | **effective range**                    | 变量能被使用的有效范围                 |
| 销毁        | **destruction / deallocation**         | 变量从内存中移除                    |
| 默认值       | **default value**                      | Java 为实例变量分配的默认初值（局部变量无默认值） |




##### 成员变量

与局部变量不同，成员变量的值在创建对象时被分配，即使未对其初始化，它们也会被赋予默认值，例如 int 类型的变量默认值为 0，boolean 类型的变量默认值为 false。



## 变量名

##### 静态变量（类变量）

- 使用驼峰命名法，应该以小写字母开头。
- 通常也可以使用大写蛇形命名法，全大写字母，单词之间用下划线分隔。
- 变量名应该是描述性的，能够清晰地表示其用途。

// 使用驼峰命名法
public static int myStaticVariable;

// 使用大写蛇形命名法
public static final int MAX_SIZE = 100;

##### 常量

- 使用全大写字母，单词之间用下划线分隔。
- 常量通常使用 `final` 修饰。

public static final double PI = 3.14;


## 访问控制修饰符

Java中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。

- **default** (即默认，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。
- **private** : 在同一类内可见。使用对象：变量、方法。 **注意：不能修饰类（外部类）**
- **public** : 对所有类可见。使用对象：类、接口、变量、方法
- **protected** : 对同一包内的类和所有子类可见。使用对象：变量、方法。 **注意：不能修饰类（外部类）**。


##### 什么是 “修饰符”（modifier）

> “修饰符” 是用来改变类、方法或变量行为的关键字。是在“声明”前面加的“形容词”。



Java 修饰符分两大类（这是关键！）

| **类型**                               | **作用**               | **常见修饰符**                                                             |
| ------------------------------------ | -------------------- | --------------------------------------------------------------------- |
| ✅ **访问控制修饰符（Access Modifiers）**      | 控制类、方法、变量的可见性（能被谁访问） | public、protected、private、（默认）                                         |
| ✅ **非访问控制修饰符（Non-access Modifiers）** | 控制类、方法或变量的行为         | static、final、abstract、synchronized、native、transient、volatile、strictfp |
![[Pasted image 20251130145941.png]]

![[Pasted image 20251130150109.png]]


![[Pasted image 20251130150130.png]]









## Java 运算符





### 数学 公式

| **方法名**                          | **考点** | **公式**                                         |
| -------------------------------- | ------ | ---------------------------------------------- |
| kilogramsToPounds                | 单位换算   | p = k * 2.20462                                |
| convertCelsiusToFahrenheit       | 温度换算   | f = 32 + (9/5)*c                               |
| getCompoundInterestValue         | 复利计算   | A = P * Math.pow((1+r), t)                     |
| getMyBMI                         | BMI 计算 | BMI = W / (H*H)                                |
| getSphereVolume                  | 球体积    | `V = (4.0/3)  *  Math.PI     * Math.pow(r, 3)` |
| getRoundedSphereVolume           | 四舍五入   | Math.round(V * 100.0)/100.0                    |
| convertTotalDaysIntoWeeksAndDays | 取整与取余  | weeks = totalDays / 7; days = totalDays % 7;   |
| findSmallerInteger               | 不用 if  | Math.min(a, b)                                 |
|                                  |        |                                                |


## Math.random

| **目标范围** | **公式**                                    | **示例** |
| -------- | ----------------------------------------- | ------ |
| 0–5      | (int)(Math.random() * 6)                  | 骰子从0开始 |
| 1–6      | (int)(Math.random() * 6) + 1              | 正常骰子   |
| 25–30    | (int)(Math.random() * (30 - 25 + 1)) + 25 | 指定区间   |
| 0.0–1.0  | Math.random()                             | 小数随机   |


#### 删掉字符

```java
public class ScramblingtheLetters {

//    每一个方法实际上都是独立的。参数之间的传输是通过 start()这里联系起来的
//     调用者，在这里就是指start()，方法之间是在 传值
    private void start(){
        String getword = getWord();
        String reArrangeWord = rearrangeWord(getword);
        String letter = getLetter();
        int getPosition = getPosition(letter , reArrangeWord);
        printNewWord(reArrangeWord);



    }




    private String getWord(){
        System.out.print("Enter a word: ");
        String word = Keyboard.readInput();
        return word;
    }



    private String rearrangeWord(String word){
//       接收word
        String letterRemaining = word;
//        空字符串准备好，下面循环拼接
        String newWord = "";

//        循环为字符长度, 随机数字为字符长度
        for(int i =0 ; i < word.length() ; i++ ){
            int randomPosition = (int)(Math.random() * letterRemaining.length());
//            拼接 charAt（index） in word
            newWord += letterRemaining.charAt(randomPosition);
//            删掉重复；如删3 , [0,3) + [4 ) --> 0 1 2 4 ⁉️链表
//            每次都是一个新的String？
            letterRemaining = letterRemaining.substring(0 ,randomPosition) + letterRemaining.substring(randomPosition +1 );
        }
//        System.out.println("newWord is : "+newWord);
        return newWord;
    }

```



“新建 Class”里输入：

`com.hardWork.practice.Practice`
- → IntelliJ 自动创建：
	•	com 文件夹
	•	hardWork 文件夹
	•	practice 文件夹
	•	Practice.java 文件
	•	顶部自动加：package com.hardWork.practice;

###### Java 的包名 = 目录结构
这是 Java 的硬性规定。
IDEA 会自动解析：
	•	最后一个 Practice 是类名
	•	前面的 com.hardWork.practice 是包名

然后就执行：

🍀 自动创建包（package）

🍀 自动创建对应的目录（folder）

🍀 自动创建类（class）


⁉️为什么这样子做：

创建src 里面的 class ： com.hardWork.practice.Practice 并点击确定，IntelliJ IDEA 将创建 com.hardWork.practice 包和 Practice 类。
✅telliJ IDEA 本身有一个**“包名识别 + 自动生成目录结构”**的智能功能。


![[Pasted image 20251123141141.png]]

## 基本语法

编写 Java 程序时，应注意以下几点：

- **大小写敏感**：Java 是大小写敏感的，这就意味着标识符 Hello 与 hello 是不同的。
- **类名**：对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 **MyFirstJavaClass** 。
- **方法名**：所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。
- **源文件名**：源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记 Java 是大小写敏感的），文件名的后缀为 **.java**。（如果文件名和类名不相同则会导致编译错误）。
- **主方法入口**：所有的 Java 程序由 **public static void main(String[] args)** 方法开始执行。


## Java修饰符

像其他语言一样，Java可以使用修饰符来修饰类中方法和属性。主要有两类修饰符：

- 访问控制修饰符 : default, public , protected, private
- 非访问控制修饰符 : final, abstract, static, synchronized

## Java 变量

Java 中主要有如下几种类型的变量  

- 局部变量
- 类变量（静态变量）
- 成员变量（非静态变量）

## Java 数组

数组是储存在堆上的对象，可以保存多个同类型变量。在后面的章节中，我们将会学到如何声明、构造以及初始化一个数组。
![[Pasted image 20251123142401.png]]
```java
public class Dog {
    String breed;
    int size;
    String colour;
    int age;
 
    void eat() {
    }
 
    void run() {
    }
 
    void sleep(){
    }
 
    void name(){
    }
}
```
一个类可以包含以下类型变量：

- **局部变量**：在方法、构造方法或者语句块中定义的变量被称为局部变量。变量声明和初始化都是在方法中，方法结束后，变量就会自动销毁。
- **成员变量**：成员变量是定义在类中，方法体之外的变量。这种变量在创建对象的时候实例化。成员变量可以被类中方法、构造方法和特定类的语句块访问。
- **类变量**：类变量也声明在类中，方法体之外，但必须声明为 static 类型。



## 构造方法
在创建一个对象的时候，至少要调用一个构造方法。构造方法的名称必须与类同名，一个类可以有多个构造方法。

![[Pasted image 20251123142632.png]]



----------------




# week 2

## This module's objectives

By the end of this module, you should be able to:

- explain the key concepts of object-oriented programming, and construct variables and methods in classes
- describe what classes and objects are, and understand the differences between them
- describe different types of visibility modifiers used for classes, methods, and variables, and their scope
- differentiate between static and instance methods in a Java program, and use these methods from common predefined Java classes such as String
- explain what local variables are and their scope
- explain how information is shared between objects and/or between methods 
	 within the same object.
- 解释面向对象编程的关键概念，并在类中构建变量和方法
- 描述什么是类和对象，并理解它们之间的区别
- 描述用于类、方法和变量的不同类型可见性修饰符及其作用域
- 区分Java程序中的静态方法和实例方法，并使用来自常见的预定义Java类（如String）的方法
- 解释什么是局部变量及其作用域
- 解释对象之间以及/或者在同一个对象内部的方法之间是如何共享信息的



你要理解 OOP 的四个核心概念：
	•	类（Class） → 模板、蓝图，定义对象的结构和行为。
	•	对象（Object） → 根据类创建出来的具体实例（“实物”）。
	•	封装（Encapsulation） → 把数据和操作数据的方法放在一个类里，并通过 private / public 控制访问。
	•	继承（Inheritance） → 子类可以继承父类的属性和方法。
	•	多态（Polymorphism） → 同一个方法名在不同对象中可以有不同表现。

👉 你要会写一个类，并在类里面放变量（数据）和方法（行为）。

![[Pasted image 20251128080303.png]]
![[Pasted image 20251128080310.png]]



### Logical operators 

![[Pasted image 20251128072538.png]]


#### 二、.equals() 是 比较内容（值）

.equals() 是对象方法，用于判断两个对象内容是否相等。

![[Pasted image 20251128073006.png]]

![[Pasted image 20251128080357.png]]

![[Pasted image 20251128080426.png]]

![[Pasted image 20251128080517.png]]

| **修饰符**       | **英文解释**                                                                                                                 | **中文解释**                          | **可访问范围** | **适用对象**     |
| ------------- | ------------------------------------------------------------------------------------------------------------------------ | --------------------------------- | --------- | ------------ |
| **private**   | The field or method can only be accessed inside the class in which it is defined.                                        | **只能在当前类内部访问**。其他类—even 子类—都不能访问。 | 当前类内      | 变量、方法        |
| **public**    | The field or method can be accessed from any class.                                                                      | **任何地方都能访问**，无论在同包还是不同包。          | 全部可见      | 类、变量、方法      |
| **protected** | The field or method can be accessed from any class within the same package or any subclass (even in different packages). | **同包内类 + 继承它的子类都能访问**。            | 同包 + 子类   | 变量、方法（不能修饰类） |
| **无修饰符**（默认）  | No explicit modifier. The field or method can be accessed from any class within the same package.                        | **默认访问权限（包级可见）**，只能在**同一个包**里访问。  | 同包类内      | 类、变量、方法      |
![[Pasted image 20251128081234.png]]




**常考陷阱题**

![[Pasted image 20251128072817.png]]
![[Pasted image 20251128072833.png]]

	•	== 比较基本类型时：比较数值
	•	== 比较对象时：比较是否是同一个对象（同一个地址）
	•	.equals()：比较对象内容是否相同（比如字符串内容）


**内部类（Inner Class）**
-  **内部类的 4 种类型（非常重要⚡️）**

| **类型**    | **定义位置**  | **是否依赖外部类实例** | **关键特征**               |
| --------- | --------- | ------------- | ---------------------- |
| **成员内部类** | 定义在类内、方法外 | ✅ 依赖          | 最常见，可以访问外部类成员          |
| **静态内部类** | 定义在类内、方法外 | ❌ 不依赖         | 相当于“嵌套类”，只访问 static 成员 |
| **局部内部类** | 定义在方法中    | ✅ 依赖          | 只在该方法里有效               |
| **匿名内部类** | 没有名字的类    | ✅ 依赖          | 用于简写一次性实现接口或继承类        |

![[Pasted image 20251130140439.png]]




## 面向对象



###  **子类（Subclass） 和 基类（Superclass / Parent Class）**
##### **子类（Subclass，也叫派生类 Derived class）**

- 使用 extends 关键字
    
- 继承父类的属性和方法
    
- 可以添加自己特有的属性和方法
`public class Dog extends Animal {}`

##### **基类（Superclass，也叫父类 Parent class）**

- 你写的一个普通类
    
- 提供属性和方法

- 供其他类继承
`public class Animal {}`

#### **protected 访问修饰符为什么和继承有关？**
#### 1：子类与基类在同一个包内

protected = public（在同包内）

也就是说：
	•	同一个包里的所有类都能访问 protected
	•	不管有没有继承关系

```
com.example
 ├── Animal.java
 └── Dog.java
```
两个类在同一个包中，protected 在两者之间就是公开可访问的。

#### 2：子类与基类不在同一个包
在不同包时：

protected 的规则变成：

只有子类本身可以访问从父类继承下来的 protected 成员。

注意：
	•	子类可以访问 自己继承下来 的 protected 成员
	•	但不能访问 父类实例 的 protected 成员

 **基类（不在同一包中）**
```
package animals;

public class Animal {
    protected int age;

    protected void eat() {
        System.out.println("Animal eats");
    }
}
```

**子类（在另一个包中）**

```
package pets;

import animals.Animal;

public class Dog extends Animal {

    public void test() {
        this.age = 5;   // ✔ 子类可以访问“继承来的” age
        this.eat();     // ✔ 子类可以调用“继承来的” eat()
    }

    public void testParent(Animal a) {
        a.age = 10;     // ❌ 不允许：不能访问父类对象的 protected 成员
        a.eat();        // ❌ 不允许：不能调用父类对象的 protected 方法
    }
}
```




**Java 位运算（bitwise operations）**
✔ 1）AND（&）

两个 1 才能得到 1，否则就是 0
（像同时按两个按钮才会亮灯）

| **A** | **B** | **结果** |
| ----- | ----- | ------ |
| 0     | 0     | 0      |
| 0     | 1     | 0      |
| 1     | 0     | 0      |
| 1     | 1     | 1      |

✔ 2）OR（|）

只要有一个 1 就是 1
（你按灯按钮 B 或者 A 都能亮灯）


✔ 3）XOR（^）

一样 = 0
不一样 = 1
（像“真假话游戏”）




**A = 60**
 0011 1100 
**B = 13**
 0000   1101


And
```
A = 0011 1100
B = 0000 1101
---------------
& = 0000 1100   （12）
```

OR（|）

只要有一个 1：
```
0011 1100
0000 1101
--------------
0011 1101   （61）
```


XOR（^）

不一样 = 1
```0011 1100
0000 1101
--------------
0011 0001   （49）
```



#### 条件运算符（?:）
条件运算符也被称为三元运算符。该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符的主要是决定哪个值应该赋值给变量。

`variable x = (expression) ? value if true : value if false`

```
 int c,d;
        c =10;
        d = (c == 1) ? 20: 30 ;
        System.out.println(d);

        d = (c == 10) ? 20: 30 ;
        System.out.println(d);
        
        
30
20        
```

#### instanceof 运算符
- 该运算符用于操作对象实例，检查该对象是否是一个特定类型（类类型或接口类型）。

instanceof 用来判断<mark class="hltr-pink">某个对象是否属于</mark>   某个类、某个父类，或者实现了某个接口。

它返回 **true 或 false**。
这是判断 **一个对象的“类型关系”** 的工具。


#### 1. 最基本的语法
`object instanceof ClassName`

`String s = "hello";`
`boolean result = s instanceof String;  // true`


#### 2. instanceof 用在哪？

✔ 判断对象是不是某个类的实例
`Dog d = new Dog();`
`d instanceof Dog   // true`


✔判断对象是不是父类类型

继承中非常有用：
`Animal a = new Dog();  // 向上转型`
`a instanceof Dog       // true`
`a instanceof Animal    // true`
因为 Dog 是 Animal 的子类。

✔ 判断对象是否实现某接口

`List< Integer> list = new ArrayList<>();`
`list instanceof List        // true`
`list instanceof ArrayList   // true`
`list instanceof Collection  // true`




![[Pasted image 20251123184911.png]]

> a instanceof Dog        // a 是属于Dog类 true
> a instanceof Animal     // a 是属于Dog类，而Dog是继承Animal类 true
> a instanceof Object     // a 确实是一个对象 ，true

`Animal a = new Dog();`
	•	右边 <mark class="hltr-lightsalmon-">new Dog() 才决定对象真正的类型</mark>
	•	左边 <mark class="hltr-pink">Animal a 只是引用类型（变量类型）</mark>

**a 是 Dog 类型对象，只是被当作 Animal 来使用**
 **“instanceof 判断的是 真实类型（右边 new 出来的）”**














-------------
# week 3

# 考试1

#### interview 1 
编写一个程序，读取一个字符串并输出每个字母“向后移动一位”的结果。

例如：
输入：I am a student
输出：g bn b tuvefou

要求：
	•	字母全部转换为小写；
	•	每个字母在字母表中向后移动 1（a→b, b→c, …, z→a）；
	•	空格不变；
	•	程序中应使用 for 循环、charAt()、Character.toLowerCase()；
	•	使用字符串拼接（result += ...）或 StringBuilder。

```java
public class EmployeeTest{

    public static void main(String[]args){
    //  每个字母都变成小写并往后移动一个字母，空格不变
        String input = "I am a student";
        String result = "";

        for(int i = 0 ;i < input.length() ;i++){
//            暂存在shore里面；
            char store = input.charAt(i);
//            判断空格
            if(store == ' ' ){
                result += ' ';
//                如果是字符， 强行小写，同时向后推一个unicode
            }else{
                store = Character.toLowerCase(store);
//     Java 中字符可以当数字加减，因为底层是 Unicode 编码。
//    ⁉️这句话在干什么？store本身就是char ，为什么还需要cast转换？
//  ✅底层上，'a' 是一个 整数（int）值 97,在 Java 里，只要你对 char、byte、short 做算术运算（+, -, *, / 等），它们会自动提升（promotion）成 int 类型来运算！
//store + 1 的结果是 int ，（cast）把结果int再转换回字符chae
//     把这个字母的 Unicode 编号 +1，然后再变回字母存回去
                store = (char)(store + 1);
//                字符串拼接操作
                result += store;
            }
        }
        System.out.println(result);
    }
}


```

### ⁉️char + String

| **概念**     | **含义**             | **典型用法**             | **在这道题中的作用**                                              |
| ---------- | ------------------ | -------------------- | --------------------------------------------------------- |
| **char**   | 表示单个字符（单个字母、空格、符号） | 'a', 'Z', ' '        | 用来“一个一个”地处理每个字母、判断空格、做 +1 计算                              |
| **String** | 表示一串字符（文本整体）       | "abc", "Hello World" | 整个输入句子（“I am a student”）是 String，用 charAt() 把它拆成 char 来操作 |

| **比较项** | String         | char              |
| ------- | -------------- | ----------------- |
| 类型      | 对象类型（Class）    | 基本数据类型（Primitive） |
| 表示      | 一串字符           | 单个字符              |
| 运算能力    | 不能参与数学运算       | 可以 +, -, ++       |
| 可变性     | 不可变（immutable） | 可变（通过赋值修改）        |
| 用途      | 保存整个句子         | 逐个处理每个字母          |
| 在本题作用   | 输入 + 拼接结果      | 遍历、判断、偏移 (+1)     |

![[Pasted image 20251129152819.png]]
![[Pasted image 20251129152921.png]]

![[Pasted image 20251129153045.png]]

#### **不能全用 String**
因为 String 是**不可变的（immutable）对象**。


### 2 、那为什么 input.charAt(i) 可以直接得到一个 char？

因为：
👉 charAt(int index) 是 String 类内置的一个方法，
它的返回类型就是 char！

![[Pasted image 20251129153335.png]]

##### 为什么 charAt() 返回的是 char 而不是 String？

**因为返回 String 太浪费内存（要创建新对象）。**
而 Java 里的 String 是不可变对象（immutable），
如果每次取一个字母都要生成新的 String，性能会非常差。















------------

# array
### 找最小数字

```java

public class Prac{
   private int anInteger(int [] integerArray){

        int lowest = 100000;

        for(int i = 0 ;i < integerArray.length ; i++){
            if(integerArray[i]  < lowest){
                lowest = integerArray[i];

            }
        }
        return lowest;
    }


    private void start(){
        int [] integerArray = new int[]{2,3,5,5,9};

        int lowest = anInteger(integerArray);
        System.out.println(lowest);

    }


    public static void main(String[]args){
        Prac s = new Prac();
        s.start();
    }
}



package prac;

public class Prac {

    private void start(){
        int [] integerArray = new int[]{4,3,6,2,7};

        int lowestInt = 1000000;

        for(int i = 0 ;i <integerArray.length; i++){
                    System.out.println(i + integerArray[i] + lowestInt);
            if(integerArray[i] < lowestInt){
                lowestInt = integerArray[i];
                    System.out.println("lowestInt " + lowestInt);
            }
        }
    }

    public static void main(String[]args){
        Prac a =new Prac();
        a.start();

    }
    }



```



![[Pasted image 20251125200456.png]]


--------------------------



## 巧克力的列子
```java
package  prac;

import java.util.Objects;
import java.util.Random;

public class Prac{
//    choc has those state;
    private int code;
    private String description;
    private double price;

    public Prac(int c ,String dec , double p){
        this.code = c;
        this.description= dec;
        this.price= p;
    }

    public int getCode(){
        return code;
    }
    public void setCode(int co){
        this.code= co;
    }

    public String getDescription(){
        return description;
    }
    public void setDescription(String de){
        this.description = de;
    }

    public double getPrice(){
        return price;
    }

    public void setPrice(double p){
        this.price = p;
    }

//    method
    public void assignRandomCode(){
        code = (int)(Math.random() * 1000);
    }

    public void print(){
        System.out.println("Description : " + description + ", price :$" + price);
    }

//            voerride translate human language
    @Override
    public String toString() {
        return "the thing is " + description +"that is good.";
    }

//    ??? 为什么permeter 是object ？
//    equal 是从object 继承 ，重写父类,规定（。。）同样签名
//    equals()两个对象是不是“内容一样”
//     instanceof = “检查类型”
    public boolean equals(Object other){
        if(other instanceof Prac){
//            把它从 Object 变成 Prac，这样才能访问 code, price
//            other通过 instanceof ,但是仍然要 cast ，规则
            Prac otherA = (Prac)other;
            return this.price == otherA.price
//                       （不能用 == 比较字符串内容）
//                   == 比较的是两个引用（地址）是否相同
//                  .equals() 才比较字符串的内容是否相同 ，但对象引用可以是同一个地址，我要比较的是“内容”
                &&this.description.equals(otherA.description)
                &&this.code == otherA.code;
        }
        return false;
    }
}

```


#### 打印sybol，奇怪的符号
```java
题目：
## Exercise Five: The Pattern Class 

In this exercise, we'll be completing the [PrintPatternProgram](./src/ictgradschool/industry/classes/printpattern/PrintPatternProgram.java) class. This class creates an instance of the `Pattern` class and calls the methods in the `Pattern` class to print different patterns.

You'll notice that there is no `Pattern` class defined yet - for this exercise, you'll need to create the class yourself, from scratch. Place it in the `printpattern` package too. This class should define a pattern.  It should consist of 2 instance variables:  the pattern symbol and the number of repetitions of the symbol. Create the `Pattern.java` file and complete the class so that `PrintPatternProgram` can print the first pattern in the output below.

Hint #1: You can create a new class in IntelliJ by right-clicking the package, and choosing New  Java Class. Name it Pattern.

Hint #2: Look at the code that’s commented out in `PrintPatternProgram` to see what methods your `Pattern` class needs to implement.

By calling the methods in the `Pattern.java` file, complete the `printPatternTwo()` method in `PrintPatternProgram` so that the second pattern is also printed, as in the output below. This method must create Pattern objects in a similar way to the `printPatternOne()` method. 


First Pattern
***************
#######.#######
~~~~~~~..~~~~~~~
~~~~~~~...~~~~~~~
~~~~~~~....~~~~~~~
~~~~~~~.....~~~~~~~
~~~~~~~......~~~~~~~
~~~~~~~.......~~~~~~~

Second Pattern
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
============............============
&&&&&&&&&&&&&..........&&&&&&&&&&&&&
&&&&&&&&&&&&&&........&&&&&&&&&&&&&&
&&&&&&&&&&&&&&&......&&&&&&&&&&&&&&&
&&&&&&&&&&&&&&&&....&&&&&&&&&&&&&&&&
&&&&&&&&&&&&&&&&&..&&&&&&&&&&&&&&&&&
&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
```



![[Pasted image 20251207103213.png]]

![[Pasted image 20251207105744.png]]

![[Pasted image 20251207105848.png]]

![[Pasted image 20251207105932.png]]

##### `Pattern andLeft = new Pattern(13 , '&');`
`andLeft.setNumberOfCharacters(andLeft.getNumberOfCharacters() + 1);`
为什么这个变量怪怪的，从对象和变量的角度讲讲？

`private double price = 0.0;`
这种price 的变量就可以直接 price++ ？
![[Pasted image 20251207140508.png]]


![[Pasted image 20251207140514.png]]
![[Pasted image 20251207140533.png]]


![[Pasted image 20251207140544.png]]

![[Pasted image 20251207140634.png]]





###### 练习6 ，手机

#### 为什么方法括号里面可以写 MobilePhone other？
![[Pasted image 20251207142244.png]]

调用的地方：
![[Pasted image 20251207142318.png]]


![[Pasted image 20251207142345.png]]

**方法的参数类型 ≠ 只能是基本类型**

可以是：
	•	int
	•	double
	•	String
	•	MobilePhone（类）
	•	Pattern（类）
	•	Medals（类）
	•	Scanner（类）
	•	List（接口）
	•	……任何对象类型都可以当参数！


![[Pasted image 20251207142419.png]]

![[Pasted image 20251207142504.png]]





##### 练习 8  老师的课程

![[Pasted image 20251207170445.png]]



![[Pasted image 20251207170523.png]]

##### 练习 9 ，电影  **Java 面向对象 + 数组 + 搜索算法**
```
Exercise Nine: Movies
For this exercise, we'll be completing code found in the movies package.

Complete the code in MovieProgram.java as in Steps 1 - 5 below, so that it produces the following output when you run the code.

Movie Collection
================
Meet the Parents (2000), 107 minutes, Director: Jay Roach
The Parent Trap (1961), 129 minutes, Director: David Swift
Alice In Wonderland (2009), 109 minutes, Director: Tim Burton
Dark Shadows (2012), 113 minutes, Director: Tim Burton
The Iron Lady (2011), 105 minutes, Director: Phylliday Lloyd
The Help (2011), 137 minutes, Director: Tate Taylor
From Russia With Love (1963), 110 minutes, Director: Terence Young
The King's Speech (2011), 118 minutes, Director: Tom Hooper
Charlie and the Chocolate Factory (2005), 115 minutes, Director: Tim Burton
Easy Rider (1969), 94 minutes, Director: Dennis Hopper
Walk the Line (2005), 136 minutes, Director: James Mangold
Kaikohe Demolition (2004), 52 minutes, Director: Florian Habicht
Brokeback Mountain (2005), 134 minutes, Director: Ang Lee
Gladiator (2000), 154 minutes, Director: Ridley Scott
The Long Voyage Home (1940), 105 minutes, Director: John Ford
Happy-Go-Lucky (2008), 118 minutes, Director: Mike Leigh
The Big Wedding (2013), 89 minutes, Director: Justin Zackham
The Intouchables (2011), 112 minutes, Director: Olivier Nakache and Eric Toledano
Searching for Sugar Man (2012), 86 minutes, Director: Malik Bendjelloul

The most recent movie is: The Big Wedding (2013), 89 minutes, Director: Justin Zackham
The longest movie is: Gladiator (2000), 154 minutes, Director: Ridley Scott

Searching for Sugar Man was directed by Malik Bendjelloul
Liberal Arts is not in the collection.
The Intouchables was directed by Olivier Nakache and Eric Toledano
Declare and construct an array of 19 Movie objects.
Write the printMoviesArray() method. This method takes an array of Movie objects as a parameter and prints all the elements as per the screenshot above. Note that the toString() method in the Movie class can be called to obtain a String containing the instance variables of a particular Movie, formatted in the required manner.
Write the getMostRecentMovie() method. This method takes an array of Movie objects as a parameter and returns a reference to the most recent Movie. Note that the isMoreRecentThan() method in the Movie class can be used to determine if a Movie is more recent than another Movie.
Write the getLongestMovie() method. This method takes an array of Movie objects as a parameter and returns a reference to the longest Movie. Note that the isLongerThan() method in the Movie class can be used to determine if a Movie is longer than another Movie.
Write the printDirector() method. This method takes 2 parameters: the name of a movie, and an array of Movie objects. The method should loop through the array searching for the movie with the name that has been passed in as a parameter. If it finds a movie with that name, it should print out the director of the movie as per the screenshot above. If it cannot find a movie with the name that has been passed in as a parameter, then it should print out “not in the collection” as per the screenshot above.
```

```java
package ictgradschool.industry.classes.movies;

public class MovieProgram {
    public void start() {

        // Step 1：构造一个可以装 19 部电影的数组（只是“盒子”，里面初始都是 null）
        Movie[] movies = new Movie[19];

        // 把具体的 Movie 对象 new 出来，放进数组对应位置
        fillMoviesArray(movies);

        // Step 2：打印整个电影集合
        printMoviesArray(movies);

        // Step 3：找到“最新”的电影（年份最大）
        Movie mostRecentMovie = getMostRecentMovie(movies);

        // Step 4：找到“时长最长”的电影（分钟数最大）
        Movie longestMovie = getLongestMovie(movies);

        // 打印上述两个结果
        printResults(mostRecentMovie, longestMovie);
        System.out.println();

        // Step 5：按片名查导演（线性搜索）
        printDirector("Searching for Sugar Man", movies);
        printDirector("Liberal Arts", movies);
        printDirector("The Intouchables", movies);

    }

    /**
     * 把 19 部电影对象 new 出来，放进 movies 数组。
     * 注意：数组 movies 在 start() 里已经分配了长度，这里只是“填充内容”。
     */
    private void fillMoviesArray(Movie[] movies) {
        movies[17] = new Movie("The Intouchables", 2011, 112, "Olivier Nakache and Eric Toledano");
        movies[6]  = new Movie("From Russia With Love", 1963, 110, "Terence Young");
        movies[14] = new Movie("The Long Voyage Home", 1940, 105, "John Ford");
        movies[9]  = new Movie("Easy Rider", 1969, 94, "Dennis Hopper");
        movies[3]  = new Movie("Dark Shadows", 2012, 113, "Tim Burton");
        movies[10] = new Movie("Walk the Line", 2005, 136, "James Mangold");
        movies[5]  = new Movie("The Help", 2011, 137, "Tate Taylor");
        movies[0]  = new Movie("Meet the Parents", 2000, 107, "Jay Roach");
        movies[7]  = new Movie("The King's Speech", 2011, 118, "Tom Hooper");
        movies[8]  = new Movie("Charlie and the Chocolate Factory", 2005, 115, "Tim Burton");
        movies[2]  = new Movie("Alice In Wonderland", 2009, 109, "Tim Burton");
        movies[4]  = new Movie("The Iron Lady", 2011, 105, "Phylliday Lloyd");
        movies[11] = new Movie("Kaikohe Demolition", 2004, 52, "Florian Habicht");
        movies[12] = new Movie("Brokeback Mountain", 2005, 134, "Ang Lee");
        movies[13] = new Movie("Gladiator", 2000, 154, "Ridley Scott");
        movies[1]  = new Movie("The Parent Trap", 1961, 129, "David Swift");
        movies[15] = new Movie("Happy-Go-Lucky", 2008, 118, "Mike Leigh");
        movies[16] = new Movie("The Big Wedding", 2013, 89, "Justin Zackham");
        movies[18] = new Movie("Searching for Sugar Man", 2012, 86, "Malik Bendjelloul");
    }

    /**
     * Step 2：打印整个电影列表
     * 利用 Movie 的 toString()，直接 System.out.println(movie) 就会自动调用 movie.toString()
     */
    private void printMoviesArray(Movie[] movies) {
        System.out.println("Movie Collection");
        System.out.println("================");

        for (int i = 0; i < movies.length; i++) {
            System.out.println(movies[i]);  // 等价于 movies[i].toString()
        }
    }

    /**
     * Step 3：从数组中找出“年份最新”的电影
     * 使用 isMoreRecentThan() 来比较两个电影谁更新。
     * 模板：max search pattern（寻找最大值的通用写法）
     */
    private Movie getMostRecentMovie(Movie[] movies) {
        // 先假设第 0 部电影是“最新”的
        Movie mostSoFar = movies[0];

        // 遍历整个数组，用每一部 movie 去和当前“最优候选”比较
        for (int i = 0; i < movies.length; i++) {
            // 如果 movies[i] 比当前 mostSoFar 更“新”，就更新最优候选
            if (movies[i].isMoreRecentThan(mostSoFar)) {
                mostSoFar = movies[i];
            }
        }
        // 循环结束后，mostSoFar 就是整个数组里“最新”的那一部电影
        return mostSoFar;
    }

    /**
     * Step 4：从数组中找出“时长最长”的电影
     * 使用 isLongerThan() 来比较两个电影谁更长。
     * 逻辑和 getMostRecentMovie 完全一样，只是比较的维度不同（lengthInMinutes）。
     */
    private Movie getLongestMovie(Movie[] movies) {
        // 假设第 0 部电影是目前最长的
        Movie longestSoFar = movies[0];

        for (int i = 0; i < movies.length; i++) {
            // 如果 movies[i] 比当前 longestSoFar 更长，就更新
            if (movies[i].isLongerThan(longestSoFar)) {
                longestSoFar = movies[i];
            }
        }
        return longestSoFar;
    }

    /**
     * 打印“最新电影”和“最长电影”的结果。
     * 注意：mostRecent / longest 直接拼接，会自动调用它们的 toString()。
     */
    private void printResults(Movie mostRecent, Movie longest) {
        System.out.println();
        System.out.println("The most recent movie is: " + mostRecent.toString());
        System.out.println("The longest movie is: " + longest.toString());
    }

    /**
     * Step 5：按名字查导演
     * movieName：要找的片名
     * movies：电影数组
     *
     * 算法：线性搜索（linear search）
     * 1. 遍历数组
     * 2. 如果有电影名字等于 movieName → 打印导演 → return 提前结束
     * 3. 遍历结束还没 return → 说明没找到 → 打印 “not in the collection”
     */
    private void printDirector(String movieName, Movie[] movies) {
        for (int i = 0; i < movies.length; i++) {
            // 字符串比较必须用 equals，而不是 ==
            if (movieName.equals(movies[i].getName())) {
                System.out.println(movieName + " was directed by " + movies[i].getDirector());
                return;  // 找到了就直接结束方法
            }
        }
        // 如果 for 循环没有任何一次满足 if，说明没有 return，代表“没找到电影”
        System.out.println(movieName + " is not in the collection.");
    }

    public static void main(String[] args) {
        new MovieProgram().start();
    }
}


--------------

package ictgradschool.industry.classes.movies;

public class MovieProgram {
    public void start() {

        // Step 1：构造一个可以装 19 部电影的数组（只是“盒子”，里面初始都是 null）
        Movie[] movies = new Movie[19];

        // 把具体的 Movie 对象 new 出来，放进数组对应位置
        fillMoviesArray(movies);

        // Step 2：打印整个电影集合
        printMoviesArray(movies);

        // Step 3：找到“最新”的电影（年份最大）
        Movie mostRecentMovie = getMostRecentMovie(movies);

        // Step 4：找到“时长最长”的电影（分钟数最大）
        Movie longestMovie = getLongestMovie(movies);

        // 打印上述两个结果
        printResults(mostRecentMovie, longestMovie);
        System.out.println();

        // Step 5：按片名查导演（线性搜索）
        printDirector("Searching for Sugar Man", movies);
        printDirector("Liberal Arts", movies);
        printDirector("The Intouchables", movies);

    }

    /**
     * 把 19 部电影对象 new 出来，放进 movies 数组。
     * 注意：数组 movies 在 start() 里已经分配了长度，这里只是“填充内容”。
     */
    private void fillMoviesArray(Movie[] movies) {
        movies[17] = new Movie("The Intouchables", 2011, 112, "Olivier Nakache and Eric Toledano");
        movies[6]  = new Movie("From Russia With Love", 1963, 110, "Terence Young");
        movies[14] = new Movie("The Long Voyage Home", 1940, 105, "John Ford");
        movies[9]  = new Movie("Easy Rider", 1969, 94, "Dennis Hopper");
        movies[3]  = new Movie("Dark Shadows", 2012, 113, "Tim Burton");
        movies[10] = new Movie("Walk the Line", 2005, 136, "James Mangold");
        movies[5]  = new Movie("The Help", 2011, 137, "Tate Taylor");
        movies[0]  = new Movie("Meet the Parents", 2000, 107, "Jay Roach");
        movies[7]  = new Movie("The King's Speech", 2011, 118, "Tom Hooper");
        movies[8]  = new Movie("Charlie and the Chocolate Factory", 2005, 115, "Tim Burton");
        movies[2]  = new Movie("Alice In Wonderland", 2009, 109, "Tim Burton");
        movies[4]  = new Movie("The Iron Lady", 2011, 105, "Phylliday Lloyd");
        movies[11] = new Movie("Kaikohe Demolition", 2004, 52, "Florian Habicht");
        movies[12] = new Movie("Brokeback Mountain", 2005, 134, "Ang Lee");
        movies[13] = new Movie("Gladiator", 2000, 154, "Ridley Scott");
        movies[1]  = new Movie("The Parent Trap", 1961, 129, "David Swift");
        movies[15] = new Movie("Happy-Go-Lucky", 2008, 118, "Mike Leigh");
        movies[16] = new Movie("The Big Wedding", 2013, 89, "Justin Zackham");
        movies[18] = new Movie("Searching for Sugar Man", 2012, 86, "Malik Bendjelloul");
    }

    /**
     * Step 2：打印整个电影列表
     * 利用 Movie 的 toString()，直接 System.out.println(movie) 就会自动调用 movie.toString()
     */
    private void printMoviesArray(Movie[] movies) {
        System.out.println("Movie Collection");
        System.out.println("================");

        for (int i = 0; i < movies.length; i++) {
            System.out.println(movies[i]);  // 等价于 movies[i].toString()
        }
    }

    /**
     * Step 3：从数组中找出“年份最新”的电影
     * 使用 isMoreRecentThan() 来比较两个电影谁更新。
     * 模板：max search pattern（寻找最大值的通用写法）
     */
    private Movie getMostRecentMovie(Movie[] movies) {
        // 先假设第 0 部电影是“最新”的
        Movie mostSoFar = movies[0];

        // 遍历整个数组，用每一部 movie 去和当前“最优候选”比较
        for (int i = 0; i < movies.length; i++) {
            // 如果 movies[i] 比当前 mostSoFar 更“新”，就更新最优候选
            if (movies[i].isMoreRecentThan(mostSoFar)) {
                mostSoFar = movies[i];
            }
        }
        // 循环结束后，mostSoFar 就是整个数组里“最新”的那一部电影
        return mostSoFar;
    }

    /**
     * Step 4：从数组中找出“时长最长”的电影
     * 使用 isLongerThan() 来比较两个电影谁更长。
     * 逻辑和 getMostRecentMovie 完全一样，只是比较的维度不同（lengthInMinutes）。
     */
    private Movie getLongestMovie(Movie[] movies) {
        // 假设第 0 部电影是目前最长的
        Movie longestSoFar = movies[0];

        for (int i = 0; i < movies.length; i++) {
            // 如果 movies[i] 比当前 longestSoFar 更长，就更新
            if (movies[i].isLongerThan(longestSoFar)) {
                longestSoFar = movies[i];
            }
        }
        return longestSoFar;
    }

    /**
     * 打印“最新电影”和“最长电影”的结果。
     * 注意：mostRecent / longest 直接拼接，会自动调用它们的 toString()。
     */
    private void printResults(Movie mostRecent, Movie longest) {
        System.out.println();
        System.out.println("The most recent movie is: " + mostRecent.toString());
        System.out.println("The longest movie is: " + longest.toString());
    }

    /**
     * Step 5：按名字查导演
     * movieName：要找的片名
     * movies：电影数组
     *
     * 算法：线性搜索（linear search）
     * 1. 遍历数组
     * 2. 如果有电影名字等于 movieName → 打印导演 → return 提前结束
     * 3. 遍历结束还没 return → 说明没找到 → 打印 “not in the collection”
     */
    private void printDirector(String movieName, Movie[] movies) {
        for (int i = 0; i < movies.length; i++) {
            // 字符串比较必须用 equals，而不是 ==
            if (movieName.equals(movies[i].getName())) {
                System.out.println(movieName + " was directed by " + movies[i].getDirector());
                return;  // 找到了就直接结束方法
            }
        }
        // 如果 for 循环没有任何一次满足 if，说明没有 return，代表“没找到电影”
        System.out.println(movieName + " is not in the collection.");
    }

    public static void main(String[] args) {
        new MovieProgram().start();
    }
}

```

![[Pasted image 20251207173910.png]]

![[Pasted image 20251207173926.png]]

![[Pasted image 20251207173942.png]]

![[Pasted image 20251207173953.png]]




#### “通用查找模式”（search pattern）
![[Pasted image 20251207174010.png]]
![[Pasted image 20251207174101.png]]






![[Pasted image 20251207174029.png]]


























----

## 创建对象

对象是根据类创建的。在Java中，使用关键字 new 来创建一个新的对象。创建对象需要以下三步：

- **声明**：声明一个对象，包括对象名称和对象类型。
- **实例化**：使用关键字 new 来创建一个对象。
- **初始化**：使用 new 创建对象时，会调用构造方法初始化对象。

> **构造函数参数不会自动变成对象属性。**
> **类里声明的属性才是最终的数据。**
> **如果构造函数参数没有赋给属性，它就废掉了。**


![[Pasted image 20251130075722.png]]


![[Pasted image 20251130080024.png]]



![[Pasted image 20251130080238.png]]

 **UML**

![[Pasted image 20251130080328.png]]

![[Pasted image 20251130081026.png]]





















#### 局部变量 Local Variables
🗂 在方法里面声明的
```
	//括号里的 int parameterVar 是 参数变量（parameter）
public void Method(int parameterVar){
    int x;
    int localVar = 10;
}
```
	•	只能在方法内部使用
	•	方法结束 → 它就消失（被销毁）
	•	❗ 必须手动初始化（不给值就报错）
	•	每次调用方法都会重新创建




#### 实例变量 Instance Variables
🗂 在类中声明，但不在方法内部：
```
public class Example {
    int instanceVar; // 实例变量
}
```
	•	属于对象，每个对象自己有一个副本
	•	对象消失 → 它才消失
	•	✔ 有默认值：
	•	int → 0
	•	boolean → false
	•	String / 对象 → null

📦 类比：

你有一个背包，你的朋友也有另一个背包。
每个人的背包（实例变量）各不相同。

 
#### 静态变量（类变量） Class Variables
🗂 用 static 声明：

```
public class Type {
   / static / int classVar;
    int instanceVar ;
}
```
特点：
	•	属于 类本身，而不是对象
	•	所有对象共享同一个值
	•	程序启动时就创建，程序结束才消失
	•	✔ 有默认值（和实例变量一致）

学校的“校规”
→ 属于整个学校，不是“某一个学生”。

就算你有 100 个 Student 对象，
校规（static 变量）只有一份，并且所有学生共享。

#### 参数变量（方法参数） Parameters
 - 方法的小括号里的变量：
`public void Method(int parameterVar){}`

特点：
	•	方法调用时由调用者传入
	•	只能在这个方法内部使用
	•	方法结束 → 消失
	•	❗ 没有默认值（必须传值）

📦 类比：

你点外卖，给外卖员你的地址（参数）。
外卖送达后，地址信息就结束生命周期。

```java
class Person {

    static int speciesCount;  <-- 类变量（所有对象共享）

    String name;              <-- 实例变量（每个对象不同）
    int age;

    public Person(String name, int age) {  <-- 参数变量
        this.name = name;
        this.age = age;
    }

    public void sayHello() {
        String greeting = "Hi";  <-- 局部变量
        System.out.println(greeting + ", I'm " + name);
    }
}
```
	•	local（局部）= 方法内部的小临时工具
	•	instance（实例）= 每个对象自己的属性
	•	class / static（类变量）= 所有对象一起共享的属性
	•	parameters（参数）= 方法调用时外部传进来的值

```java
package com.hardWork.practice;

public class Type {
//
    private int instanceVar;
    private static int staticClassVar;

    //括号里的 int parameterVar 是 参数变量（parameter）
    public void method(int parameterVar) {
        int localVar = 10;

        instanceVar =localVar ;
        staticClassVar = parameterVar ;

        System.out.println("成员变量: " + instanceVar);
        System.out.println("staticClassVar: " + staticClassVar);
        System.out.println("parameterVar : " + parameterVar);
        System.out.println("localVar : " + localVar);


    }
public static void main(String[]args){
        Type a = new Type();
        a.method(30);

}
}



成员变量: 10
staticClassVar: 30
parameterVar : 30
localVar : 10
```


##### parameter

- **值传递：** 在方法调用时，传递的是实际参数的值的副本。当参数变量被赋予新的值时，只会修改副本的值，不会影响原始值。Java 中的<mark class="hltr-pink">基本数据</mark>类型都采用值传递方式传递参数变量的值。
    
- **引用传递：** 在方法调用时，传递的是实际参数的引用（即内存地址）。当参数变量被赋予新的值时，会修改原始值的内容。Java 中的<mark class="hltr-pink">对象类型</mark>采用引用传递方式传递参数变量的值。

##### instance

成员变量的值在创建对象时被分配，即使未对其初始化，它们也会被赋予默认值

成员变量可以通过对象访问，也可以通过类名访问（如果它们是静态成员变量）


##### static
###### 静态变量的使用场景
静态变量通常用于以下场景：

- 存储全局状态或配置信息
- 计数器或统计信息
- 缓存数据或共享资源
- 工具类的常量或方法
- 单例模式中的实例变量

静态变量的访问权限与实例变量不同，因为静态变量是与类相关的，不依赖于任何实例。

| **类型**            | **属于谁？** | **怎么访问？**     | **有什么影响？**   |
| ----------------- | -------- | ------------- | ------------ |
| **静态变量 (static)** | 属于类      | ClassName.var | 不需要对象，全局共享一份 |
| **实例变量**          | 属于对象     | obj.var       | 每个对象一份，不共享   |
- 因为两者的“归属不同”，所以它们的访问方式不同：
- 静态变量 —— 由类访问
		你可以在不创建对象的情况下访问：
		也可以通过对象访问（不推荐）：






![[Pasted image 20251125200506.png]]
![[Pasted image 20251125200529.png]]




## 作业
```java
package ictgradschool.industry.arrays.basics;

public class ArrayBasics {

    public int getSumOfPositiveIntegers(int[] integerArray) {
        // TODO: complete your code here
        int sum = 0;
        for(int i = 0 ;i <integerArray.length; i++){
            if(integerArray[i] > 0){
                sum = sum+ integerArray[i];
            }else{
                break;
            }
        }
        return sum;
    }

    public String getLongestString(String[] stringArray) {
        // TODO: complete your code here

        if(stringArray.length == 0){
            return null;
        }
//        初始化为第一个元素，从数组的第一个元素开始，把它当成“目前最好的答案”，然后用循环逐个比较，如果找到更好的就替换。
            String longest = stringArray[0];

        for(int i = 0; i < stringArray.length ;i++) {
            if(stringArray[i].length() > longest.length()) {
                longest = stringArray[i];
            }
        }
        return longest;
    }

    public void start() {
        int[] integerArray = new int[]{3, 56, 23, -4, -12, 34, 2, -7};
        int totalOfPositiveIntegers = getSumOfPositiveIntegers(integerArray);
        System.out.println("The sum of all positive integers is: " + totalOfPositiveIntegers);

        String[] animalArray = new String[]{"cat", "mouse", "pelican", "donkey", "dog", "horse"};
        String longestString = getLongestString(animalArray);
        System.out.println("The longest String in the array is: " + longestString);
    }

    public static void main(String[] args) {
        ArrayBasics program = new ArrayBasics();
        program.start();
    }

}

```
## **数组万能模板（Arrays）**

#### **求和 / 找最大 / 找最小 / 找最长字符串 / 统计 / 查找**

![[Pasted image 20251125201247.png]]
![[Pasted image 20251125201303.png]]
![[Pasted image 20251125201323.png]]

![[Pasted image 20251125215952.png]]




```java
public class ClassName {

    // ① Instance variables
    private String name;
    private double price;
    private boolean active;

    // ② Constructor
    public ClassName(String name, double price, boolean active) {
        this.name = name;
        this.price = price;
        this.active = active;
    }

    // ③ Getters
    public String getName() { return name; }
    public double getPrice() { return price; }
    public boolean isActive() { return active; }

    // ④ Setters
    public void setName(String name) { this.name = name; }
    public void setPrice(double price) { this.price = price; }
    public void setActive(boolean active) { this.active = active; }

    // ⑤ Boolean comparison method
    public boolean isMoreExpensiveThan(ClassName other) {
        return this.price > other.price;
    }

    // ⑥ toString()
    public String toString() {
        return name + " costs $" + price;
    }
}
```


### <mark class="hltr-lightsalmon-">问题</mark>

#### 这两种有什么区别？
```
int[] arrayA = {1, 2, 3, 4, 5, 6};
int[] arrayB;
arrayB = arrayA;


int[] arrayA = {1, 2, 3, 4, 5, 6};
// Create a new array with the same size as arrayA
int[] arrayB = new int[arrayA.length];
// Assign all the values from arrayAto arrayB
for (int i = 0; i < arrayB.length; i++) {
arrayB[i] = arrayA[i];
}
```

![[Pasted image 20251126105605.png]]
![[Pasted image 20251126105618.png]]



![[Pasted image 20251126105637.png]]

![[Pasted image 20251126105646.png]]


| **写法**          | **是否新建数组？** | **是否两个数组互相影响？** |
| --------------- | ----------- | --------------- |
| arrayB = arrayA | ❌ 否         | ❌ 会互相影响（同一块内存）  |
| 逐个复制            | ✅ 是         | ✅ 不会互相影响（完全独立）  |


![[Pasted image 20251126105801.png]]

#### 静态方法 static method

![[Pasted image 20251126112620.png]]


### 我们要 在数组里寻找某个“最值”（最小、最大、最频繁）。

找“最值”的算法套路永远是：

✔️ Step 1：先假设第一个元素是答案

（这是唯一安全、不会出错、不会空指针的写法）

然后在 loop 里不断修正。

✔️ Step 2：遍历数组，与这个“假设值”比较
![[Pasted image 20251126144928.png]]

# **为什么初始化必须是 values[0]？**

  

因为：

- 它保证一定是数组里的真实值
    
- 不会影响比较结果
    
- 无论数组内容是什么都适用
    
- 不会出 bug，不会出错
    

这是算法里最经典、最标准的写法。


-----


⁉️⁉️

```
/**
     * Q4. Complete the method findMostFrequentInteger that returns the most frequently occurring number in an integer
     * array. For example, given an int array: {1, 2, 3, 4, 5, 1}, the method will return 1 as the most frequently
     * occurring number.
     * <p>
     * If there are more than one most frequently occurring number, then return the smallest number from the most
     * frequently occurring numbers. For example, given an int array {2, 3, 3, 2, 4, 5, 4}, the method should
     * return 2 as the most frequently occurring number.
     * <p>
     * You may assume that there is always at least one value in the given array.
     *
     *    需要哪些变量， 需要什么结构？
     * 1. 找 most frequently   出现次数最多的数字
     * 2. if( 多个freq)
     * 3.    找smallest      如果出现次数一样多 → 选数字更小的
 *          2 for
     *
     */
    public int findMostFrequentInteger(int[] values) {

        //Answer here

            int mostFrequentNumber = values[0];
            int highestFrequency = 0;

            for(int i  = 0 ;i < values.length ; i++){
                int currentNumber = values[i];
                int count = 0;
                for(int j = 0; j< values.length; i++){
                    if(values[j] == currentNumber){
                        count ++;
                    }
                }
//             比较条件  如果两个数字出现次数一样多，取数字更小的那一个。
//            如果当前数字出现次数比之前记录的最高次数还多   ｜｜ 如果出现次数一样多 ，那就选数字更小的那个
                if(count > highestFrequency){
                    highestFrequency = count ;
                    mostFrequentNumber = currentNumber;
                }else if(count == highestFrequency && currentNumber < mostFrequentNumber){
                mostFrequentNumber = currentNumber ;
                }
            }
        return mostFrequentNumber;
        //
    }

```
🔥 Arrays 所有常考算法套路总结（极其有用）

🔥 CodeRunner 全部题目最简单模板+自动记忆口诀


## 作业
```java
package ictgradschool.industry.arrays.coderunner;

import java.util.zip.CheckedInputStream;

/**
 * Please run the TestCodeRunner class to check your answers.
 *
 * There are five exercises in this class. They are ordered roughly in increasing order of difficulty.
 * You can do them in any order you like.
 * <p>
 * You may modify the code in between the comments: // Answer here // . Do not modify other parts of the code.
 * <p>
 */
public class CodeRunner {
    /**
     * Q1. Complete the method sumArray that returns the sum of values in a given int array.
     * For example, sumArray(new int[]{1, 2 ,3}) should return 6 as the sum.
     */
    public int sumArray(int[] values) {
        //Answer here
        int sum = 0 ;
        for(int i =0; i < values.length ; i++){
            sum += values[i];
        }
        return sum;
        //
    }

    /**
     * Q2.Complete the method getBiggestValue that returns the
     * maximum value from a given int array.
     * For example, getBiggestValue(new int[]{0, 12 ,101}) should return 101 as the biggest value.
     */
    public int getBiggestValue(int[] values) {
        // Answer here
        int biggest = values[0];
        for(int i = 0 ; i< values.length ; i++){
            if( biggest < values[i]){
                biggest = values[i];
            }
        }
        return biggest;
        //
    }

    /**
     * Q3. Complete the method countOnes that returns the number of values that
     * are equal to one from a given int array.
     * For example, countOnes(new int[]{0, 1 ,1}) should return 2 as the number of ones from the given array.
     *   找 1 统计最常出现的数字
     */
    public int countOnes(int[] values) {
        // Answer here
        int one = 0;
        for(int i = 0 ;i < values.length ; i++){
            if(values[i] == 1) one++;
        }
        return one;
        //
    }

    /**
     * Q4. Complete the method findMostFrequentInteger that returns the most frequently occurring number in an integer
     * array. For example, given an int array: {1, 2, 3, 4, 5, 1}, the method will return 1 as the most frequently
     * occurring number.
     * <p>
     * If there are more than one most frequently occurring number, then return the smallest number from the most
     * frequently occurring numbers. For example, given an int array {2, 3, 3, 2, 4, 5, 4}, the method should
     * return 2 as the most frequently occurring number.
     * <p>
     * You may assume that there is always at least one value in the given array.
     *
     *    需要哪些变量， 需要什么结构？
     * 1. 找 most frequently   出现次数最多的数字
     * 2. if( 多个freq)
     * 3.    找smallest      如果出现次数一样多 → 选数字更小的
 *          2 for
     *
     */
    public int findMostFrequentInteger(int[] values) {

        //Answer here

            int mostFrequentNumber = values[0];
            int highestFrequency = 0;

            for(int i  = 0 ;i < values.length ; i++){
                int currentNumber = values[i];
                int count = 0;
                for(int j = 0; j< values.length; j++){
                    if(values[j] == currentNumber){
                        count ++;
                    }
                }
//             比较条件  条件1：出现次数更多
//                      条件2：出现次数一样多，但数字更小
                if(count > highestFrequency){
                    highestFrequency = count ;
                    mostFrequentNumber = currentNumber;
                }else if(count == highestFrequency && currentNumber < mostFrequentNumber){
                mostFrequentNumber = currentNumber ;
                }
            }
        return mostFrequentNumber;
        //
    }


    /**
     * Q5. Complete the method computeFibonacci that returns an int array of Fibonacci sequence where the size of which
     * is controlled by a given positive integer number.
     * <p>
     * A Fibonacci sequence is a series of numbers where the next number is the sum of the previous numbers. For example,
     * if the method is given the number 6, it will return an int array with size 6 consisting the following numbers:
     * {1, 1, 2, 3, 5, 8}
     * <p>
     * If the size is 0, the method should return null.  // size == 1
     */
    public int[] computeFibonacci(int size) {
        //Answer here
        if(size == 0) {
            return null;
        }

        int [] sum = new int[size];

        if(size == 1){
            sum[0] = 1;
            return sum ;
        }
        sum[0] = 1;
        sum[1] = 1;
//       递推
        for(int i = 2 ; i < sum.length ;i++){
            sum[i] = sum[i -1] + sum[i -2];
        }
        return sum;
        //
    }
}



```

### 总结
![[Pasted image 20251126161920.png]]


![[Pasted image 20251126161930.png]]


![[Pasted image 20251126161941.png]]

![[Pasted image 20251126162001.png]]
![[Pasted image 20251126162021.png]]

![[Pasted image 20251126162031.png]]
![[Pasted image 20251126162040.png]]
![[Pasted image 20251126162050.png]]

| **题目** | **考点**         | **关键知识**                         |
| ------ | -------------- | -------------------------------- |
| Q1     | 遍历数组求和         | for + index + return sum         |
| Q2     | 找最大值           | 初始值 = 第一个元素                      |
| Q3     | 计数             | if(values[i] == 1)               |
| Q4     | 双重循环、频率统计、选最小值 | count、highestFrequency、tie-break |
| Q5     | 递推、特殊情况处理      | size == 0/null、size== 1、 公式      |





# test 1

```
Instructions
Topics covered: Labs 01–03.
Duration: 60 minutes (how long the test has been designed to take)
Available: 75 minutes (how much time you have to work on the test, to allow for technical difficulties)
Approach your work with honesty and integrity.
The test is open book. You may use any resources provided in this course as well as any online resources. However, you are prohibited from using generative artificial intelligence text and art generation software, such as ChatGPT and Copilot, in this test. You are expected to complete this test without substantial assistance from others, including automated tools. Failure to follow instructions will receive a mark of 0 for the entire test.
You must use one of the lab computers in 301-162 to take the test.
You may not use any translation tools.
Please submit your test before the due date.
IMPORTANT: Make sure to read the instructions carefully before attempting each question.
This quiz was locked 28 Nov at 12:00.
Attempt history
Attempt	Time	Score
LATEST	Attempt 1	Time:75 minutes	Score:44 out of 60
Score for this quiz: 44 out of 60
Submitted 28 Nov at 11:25
This attempt took 75 minutes.
 
Correct answer
Question 1
2 / 2 pts
Integer is a primitive type.

  True 
  False 
 
Correct answer
Question 2
2 / 2 pts
void is a primitive type.

  True 
  False 
 
Unanswered
Question 3
0 / 2 pts
Any primitive type can be casted to any other primitive type.

  True 
  False 
 
Correct answer
Question 4
2 / 2 pts
You can write multiple return statements in the same method.

  True 
  False 
 
Correct answer
Question 5
2 / 2 pts
Math.random() is an instance method.

  True 
  False 
 
Correct answer
Question 6
2 / 2 pts
Math.random() returns a double.

  True 
  False 
 
Correct answer
Question 7
2 / 2 pts
What is the value of GREETING after the code snippet below is executed?

2025ly-test1-greeting.png

  Error, we cannot assign a new value to the final variable GREETING once it has been initialised 
  "Hello David" 
  
Error, the final variable GREETING needs to be declared and initialised at the same time, i.e. final String GREETING = "Hello world";

  "Hello world" 
 
Wrong answer
Question 8
0 / 2 pts
What is the largest possible value of (int) Math.random() * 10 + 1?

  1 
  10 
  9 
  11 
 
Correct answer
Question 9
2 / 2 pts
Suppose name is a string variable with value "teamrocket". What is the value of name.substring(3, 5) + name.substring(6, 8)?

  mrocke 
  amrock 
  amoc 
  mrck 
 
Correct answer
Question 10
2 / 2 pts
Suppose bell is an integer variable with value 29 and salmon is a string variable with value "29". Which of the following statements are true?

  (int) salmon can be used to convert salmon to integer 
  Integer.parseInt(salmon) can be used to convert salmon to integer 
  bell.toString() can be used to convert bell to string 
  "" + bell can be used to convert bell to string 
 
Unanswered
Question 11
0 / 2 pts
Suppose word is a string variable with value "eerie". Which of the following strings are equal to word.substring(0, 1)?

  
word.substring(1, 2)

  
word.substring(1, 1)

  
word.substring(0)

  
word.substring(4)

 
Correct answer
Question 12
2 / 2 pts
Which of the following statements are true after the code snippet below is executed?

2025ly-test1-helloworld.png

  string2 is equal to "hello.world" 
  string1 is equal to string2 
  string2 is equal to "helloworld" 
  string1 is equal to "hello." 
 
Question 13
2 / 3 pts
Fill in the blanks so that the following code snippet prints out all even numbers between 2 and 10 (both 2 and 10 should be printed out).

2025ly-test1-forblank-1.png

 

Answer 1: 
int i = 10

Answer 2: 
i >= 0

Answer 3: 
i % 2 != 0

Answer 1:
int i = 10
Answer 2:
i >= 0
i > 0 
i > 1 
i >= 2 
Answer 3:
i % 2 != 0
i % 2 == 1 
!(i % 2 == 0) 
0 should not be printed
 
Wrong answer
Question 14
1 / 2 pts
Suppose x is an integer variable. Convert the statement below into a boolean expression.

x is -1, or x is an even number less than 60

if(x = -1   ||  (x  % 2 == 0 )  < 60 ){}
x == -1 || (x % 2 == 0 && x < 60) 
The idea is correct but some syntax mistakes
 
Wrong answer
Question 15
0 / 2 pts
Suppose x is an integer variable. Convert the statement below into a boolean expression.

x is a number that ends with 5, but x is not 15 or 25.

if( x.charAt(x.length() - 1) = '5'  && (x != 15  || x ! = 25){}
x % 10 == 5 && x != 15 && x != 25 
You can't use charAt() for integers.
 
Question 16
2 / 2 pts
In your own words, explain one difference between a static method and an instance method.

Your answer:
static method : the method that are called using the name of a class .

 

 

instance method: the method that "belong" to the object to do things. And need to construct an object before calling an instance method.

A static method must be called directly from a class, e.g. Math.min(). To call an instance method, you first need to create an instance and then call the method from that.

 
Question 17
2 / 4 pts
What is the output when the following code snippet is executed? Explain why this is the case.

2025ly-test1-explain.png

Your answer:
print a simple string  : 5 2.5 +5 2.5

 the result will beacuse the String + other number will beacome the string .

b stores the value of 2.0. In Java, a / 2 would give us the value 2 as integer divided integer would return an integer. The value after the decimal place is therefore truncated. Since b expects to store a double value, the value 2 is turned into 2.0.

We perform the expression inside the System.out.println statement from left to right. The first + sign is simply adding two numbers together. Then, the sum of a and b is joined to the String "+". At this stage, the output is "7.0+". This in turn converts the remaining + signs into String concatenation. Therefore, the output at the end is "7.0+52.0".

 
Question 18
3 / 4 pts
The following method contains four mistakes that cause compilation errors. Identify each mistake and state how each mistake should be fixed.

2025ly-test1-printsum-1.png

Your answer:
1.  in paramenter  ; change to , 

 2. in second print  sum should initialisze first or before call it.

3. a and b no value ,should enter real number into the pragramm.

4.no else conditon , and no return value.

return type should be void, not int
parameters should be separated by comma, not semicolon
sum needs to be declared before it's used in the second print statement
if statement needs to use ==, not =
 124 are correct. If statements don't need to have an else condition. a and b do have a value because they are parameters.
 
The following three questions relate to the doSomething() method below. (Assume that input will always contain at least 2 characters and never be null.)

2025ly-test1-ijloop.png

 
Question 19
2 / 2 pts
There is a mistake in the method that could potentially cause a run-time error. Identify the mistake and state how the mistake should be fixed.

Your answer:
in second for loop : count is wrong i  ,shoule be j .

  for(ing j = 0 ; ...... ; j ++){

}

i

 i would plus 2 ,and j no plus each run - time;

The second loop increments i instead of j. It should be changed to j++.

 
Question 20
1 / 2 pts
Assuming the mistake is NOT fixed, give an example of a string input which would not cause any error.

Your answer:
" "

 

input a space ,return false directly without compiler mistake ;

just pass away the 2 for loop;

"aa"

 Technically you are right, but for this question assume input length is at least 2.
 
Question 21
4 / 4 pts
Assuming the mistake IS fixed, explain what the method does.

Your answer:
2 for boolean loop 

i loop is outside  , and j loop is inside ; both a different index in a same string which is passed from outside of method.

at the end of the programme ,the result will return the false  or true .

true condition : i and j in different index AND  the character represented by the i and j  are same .

 dod

d[ i ] o d[ j ]  , return ture ;

ouerwise ,false ;

The method checks whether any two letters are the same in the string. For example, this method would return true for "adapt" (because there are two 'a's), but false for "alien" (because each letter appears once only).

 
Question 22
3 / 3 pts
What is the output when the main method of this class is executed? Explain why this is the case.

2025ly-test1-fruit.png

Your answer:
"The fruit is pineapple"

"The fruit is apple"

"The fruit is apple"

 

fruit1 fruit2,fruit3  are both object belong Fruit class

fruit1 is a unique.

 fruit3 = fruit2 are same the memory address ,  fruit3  is assigned  fruit2 ,fruit2 set itslfe name ,so  fruit3 change  same time.

 

The fruit is pineapple

The fruit is apple

The fruit is apple

fruit2 and fruit3 are the same object because of the assignment statement Fruit fruit3 = fruit2;. So when the name of fruit2 is set to "apple", this becomes the name for fruit3 as well.

 
Question 23
6 / 8 pts
Write a method that asks the user for input until the user enters the empty string (""), then prints all of the previous inputs joined together.

The output should look something like this:

2025ly-test1-facetious.png

Your answer:
while(true){

System.out.println("Enter world : ");
 String a=
String.parseString(Keyboard.readInput());
            if (a = '' ") {
          
            }
 return System.out.println("Enter world : ");

}

return false;

public void printUserInputs() {

    String input = "abc";

    String total = "";

    while (input.length() > 0) {

        System.out.print("Enter word: ");

        input = Keyboard.readInput();

        total += input;

    }

    System.out.println(total);

}

 Almost correct. You need another string variable to keep track of the final result.
```


-----





# [[# week 4]]

### Arrays and classes

### 作业
### pokeman lab

#### **数组里放了对象，怎么取出对象的某个属性或方法？**

数组里放的是 **对象（object）**
对象里面有 **属性（field）** 和 **方法（method）**

所以要访问：
> **先取出数组里的对象，再访问对象的属性或方法**


![[Pasted image 20251129182902.png]]
![[Pasted image 20251129182941.png]]


![[Pasted image 20251129182949.png]]

![[Pasted image 20251129183005.png]]


![[Pasted image 20251129183027.png]]
> **数组通过 `[index]` 取到对象，**

> **对象通过 . 来取属性或方法。**

数组名`[ 索引 ].属性`
数组名`[ 索引 ].方法()`

```java
private void printPokemonsGreetings(Pokemon[] pokemons) {
    // TODO: Complete the method according to the test instructions
    for (int i = 0; i < pokemons.length; i++) {
        System.out.println("I am " + pokemons[i].name + ", my current level is " + pokemons[i].level);
    }
}
```

### 向下转型（downcasting） = 把父类类型的引用，强制当成子类类型来使用。

![[Pasted image 20251129204639.png]]

![[Pasted image 20251129204651.png]]

![[Pasted image 20251129205504.png]]



![[Pasted image 20251129205513.png]]


![[Pasted image 20251129205531.png]]

![[Pasted image 20251129205553.png]]

![[Pasted image 20251129205827.png]]

```java
package ictgradschool.industry.inheritance.pokemons;

public class PokemonGenerator {

    // This is the main method
    // DO NOT EDIT!

    /*
    Greetings from Pokemons
====================
I am Pikachu, my current level is 3
I am Psyduck, my current level is 3
I am Charmander, my current level is 2
I am Squirtle, my current level is 5
I am Electrode, my current level is 3
====================

Electric Pokemons show-off time
-------------------------------
I say "Pika pika" when I attack!
I say "ts...ts...ts...Electrode" when I attack!
-------------------------------

Random attack time!
-------------------
Not enough experience for Squirtle!
Not enough experience for Electrode!
Not enough experience for Electrode!
-------------------

Pokemons' status after the attacks
==================================
I am Pikachu, my current level is 3
I am Psyduck, my current level is 1
I am Charmander, my current level is 1
I am Squirtle, my current level is 1
I am Electrode, my current level is 3
     */



    public static void main(String[] args) {
        PokemonGenerator pokemonGenerator = new PokemonGenerator();
        pokemonGenerator.start();
    }

    // This is the start of the PokemonGenerator
    // DO NOT EDIT!
    public void start() {
        // Getting an array of Pokemons with random levels
        Pokemon[] pokemons = createPokemons();



        System.out.println("Greetings from Pokemons");
        System.out.println("====================");

        // Printing each Pokemon with its own greeting from the given array
        printPokemonsGreetings(pokemons);

        System.out.println("====================");
        System.out.println();

        System.out.println("Electric Pokemons show-off time");
        System.out.println("-------------------------------");

        // Printing each electic type Pokemon from the given array
        printElectricPokemons(pokemons);

        System.out.println("-------------------------------");
        System.out.println();

        System.out.println("Random attack time!");
        System.out.println("-------------------");

        // Any three random Pokemons from the given array
        // will attack three other random Pokemons
        // Note that the Pokemon will not attack itself
        randomAttacks(pokemons);

        System.out.println("-------------------");
        System.out.println();

        System.out.println("Pokemons' status after the attacks");
        System.out.println("==================================");
        printPokemonsGreetings(pokemons);
    }



//    I am Pikachu, my current level is 3
//    I am Psyduck, my current level is 3
//    I am Charmander, my current level is 2
//    I am Squirtle, my current level is 5
//    I am Electrode, my current level is 3

//     five different Pokemon objects and assign them to the pokemons array
    private Pokemon[] createPokemons() {
        // TODO: Complete the method according to the test instructions.
        //  You may modify the code inside this method.
// Java 数组可以放“对象”，但必须放对象引用（reference）
// 但是 new Pokemon[5];每个格子都准备放一个 Pokémon 对象。（对象必须用 new 创建）

        Pokemon[] pokemons = new Pokemon[5];

        pokemons[0] = new Pikachu("Pikachu" ,generateRandomLevel());
        pokemons[1] = new Psyduck("Psyduck" ,generateRandomLevel());
        pokemons[2] = new Charmander("Charmander" ,generateRandomLevel());
        pokemons[3] = new Squirtle("Squirtle" ,generateRandomLevel());
        pokemons[4] = new Electrode("Electrode" ,generateRandomLevel());

        return pokemons;
    }



    private int generateRandomLevel() {
        // TODO: Complete the method according to the test instructions.
        //  You may modify the code inside this method.
//    随机生成 1 - 5 ,+1是去掉 0 ，满足 （1 - 5）；
        int level = (int)(Math.random() * 5) + 1;
        return level;
    }




//数组里放了对象，取出对象的某个属性或方法 ,
//数组里放的是 对象（object），对象里面有 属性（field） 和 方法（method），所以要访问：先取出数组里的对象，再访问对象的属性或方法
//    这里用到get ，但是modifier 是protected ，所以ok
    private void printPokemonsGreetings(Pokemon[] pokemons) {
        // TODO: Complete the method according to the test instructions
        for(int i = 0 ; i < pokemons.length;i++) {
            System.out.println("I am " + pokemons[i].getName() + ", my current level is " + pokemons[i].getLevel());
        }
    }


//实现的是INoise接口，但是pokeman的父类没有这个方法 ，需要 create 接口的 对象 ，然后 强制转换
//判断一个对象是不是某个类 的实例：   instanceof
//如何打印声音？为什么要写 \"？（转义的概念）✅有双引号啊 ，（接口 INoise 怎么用）
//需要一个变量 强制转型 ，转的是Inoise的类，向下转型（downcasting） = 把父类类型的引用，强制当成子类类型来使用。
    private void printElectricPokemons(Pokemon[] pokemons) {
        // TODO: Complete the method according to the test instructions.
        for(int i =0 ; i < pokemons.length ; i++) {
            if (pokemons[i].type instanceof ElectricType) {
                INoise sound = (INoise)pokemons[i];
                System.out.println(" I say \"" +sound.makeNoise() +"\"when I attack!");
            }
        }
    }


//    -------------------
//Not enough experience for Squirtle!
//Not enough experience for Electrode!
//Not enough experience for Electrode!
//-------------------
//
//Pokemons' status after the attacks

// 调用leuel up /  attack
    private void randomAttacks(Pokemon[] pokemons) {
        // TODO: Complete the method according to the test instructions.
        //  You may modify the code inside this method.

        for(int i = 0 ;i < 3 ; i++){
            int Attack = (int)(Math.random() * 5);
            int underAttacked = (int)(Math.random() * 5);
//❌ if ,无法避免第二次重复 ❌Math.random() * 5 写死随机数 ，应该用 array。length
            while(Attack == underAttacked){
                underAttacked = (int)(Math.random() * 5);
            }

//            需要调用attack(传进被攻击的pokeman)
            pokemons[Attack].attack(pokemons[underAttacked]);
        }
    }
}


```


#### Exercise Four: Polymorphism and Static
```java

You can complete this exercise on paper.

1. What is the output when you run the following code? 

```java
//  一个子类对象创建时，会自动先执行父类构造器，再执行自己的构造器。
//  static 共享
public class SuperClass { 
    public int x = 10; 
    static int y = 10;
//    静态字段 y = 10（所有 SuperClass 和 Test1 共用一份）
 
    SuperClass() { 
        x = y++; 
    } 
//    y 先把自己的的旧值赋给 x，然后 y 增加 1;
//    此时  x任然是10 ，y 之后+ 1  = 11； 
 
    public int foo() { 
        return x; 
    } 
 
    public static int goo() { 
        return y; 
    } 
} 
 
public class Test1 extends SuperClass { 
    int x2= 20; 
    static int y2 = 20; 
 
// t自动执行super的construtor ，notice ： x还是先被y 赋值= 11 。 y 自己 + 1 = 12
// 后面t1 调用的时候，sup数值已经变了
    Test1() { 
        x2 = y2++;
    } 
//     20 = 21
 
    public int foo2() { 
        return x2; 
    } 
 
    public static int goo2() { 
        return y2; 
    } 
 
    public static void main(String[] args) { 
        SuperClass s1 = new SuperClass(); 
// 一个子类对象创建时，会自动先执行父类构造器，再执行自己的构造器。
// t1 执行 SuperClass() 构造器，此时 y 已经是 11 了（因为 s1 改过）,调用的那一刻，数值再次变化  x 被复制 =11 ，y自增 12；
        Test1 t1 = new Test1(); 
        System.out.println("The Base object"); 
        System.out.println("S1.x = " + s1.x); 10
        System.out.println("S1.y = " + s1.y); 11
        System.out.println("S1.foo() = " + s1.foo());10 
        System.out.println("S1.goo() = " + s1.goo()); 11
        System.out.println("\nThe Derived object"); 
        System.out.println("\nInherited fields");
//        (继承来的字段)
//      t1对象出现的那一刻，自动调用super ， x y 在此改变👆，上面备注
        System.out.println("T1.x = " + t1.x);  11  ❌10
        System.out.println("T1.y = " + t1.y);  12   ❌11
        System.out.println("T1.foo() = " + t1.foo());  11
        System.out.println("T1.goo() = " + t1.goo()); 12
//                子类自己新增的字段
        System.out.println("\nThe instance/class fields"); 
        System.out.println("T1.x2 = " + t1.x2);  20
        System.out.println("T1.y2 = " + t1.y2); 21 
        System.out.println("T1.foo2() = " + t1.foo2()); 20
        System.out.println("T1.goo2() = " + t1.goo2()); 21
    } 
}
```
2. What is the output when you run the following code? The `SuperClass` will remain the same.

```java

//static 看变量的类型，普通方法看对象的真实类型
//static 字段完全不看对象，只看“引用类型（左边的类型）” 
// static y ， Test1 有自己的版本，SuperClass 有自己的版本：它们互不影响，各用各的。

//public class SuperClass {
//    public int x = 10;
//    static int y = 10;
//    SuperClass() {x = y++;}
//    public int foo() {return x;}
//    public static int goo() { return y;}}


public class Test1 extends SuperClass { 
    static int x = 15; 
    static int y = 15; 
    int x2= 20; 
    static int y2 = 20; 
 
// SuperClass(){x = y++ };   
    Test1() { 
        x2 = y2++; 
    } 
 
    public int foo2() { 
        return x2; 
    } 
 
    public static int goo2() { 
        return y2; 
    } 
 
    public static int goo(){ 
        return y2; 
    } 
 
    public static void main(String[] args) { 
        
//左边 / 右边”
//s2 这个变量的类型是 SuperClass（老师叫：静态类型 / 编译期类型）
//真正 new 出来的对象，是 Test1 类型（老师叫：动态类型 / 运行时类型）
//虽然右边 new 的是 Test1 对象，但 s2 的类型是 SuperClass，所以：访问 static 字段，看左边 ，调用 static 方法 ，看左边
        
        SuperClass s2 = new Test1(); 
        System.out.println("\nThe static Binding"); 
        System.out.println("S2.x = " + s2.x); 
        System.out.println("S2.y = " + s2.y); 
        System.out.println("S2.foo() = " + s2.foo()); 
        System.out.println("S2.goo() = " + s2.goo()); 
    } 
} 
```

3. To which class is the method `s2.goo()` called?
```java
//   static int goo , SuperClass

4. What is the static type of variable `s2`?
//   SuperClass s2  

5. Are we able to make a call to method `foo2()` from variable s2?
//   不能调用（编译错误）
// s2 的静态类型是 SuperClass ,SuperClass 里没有 foo2()

6. What is the result from the following line of code?
//编译错误（父类不能赋给子类）
    `Test1 t2 = new SuperClass();`

7. What is the result from the following line of code?
⁉️pokeman inoise的列子？ 
//强行把父类变成子类，不可能
    `Test1 t2 = (Test1) new SuperClass();`

⁉️⁉️INoise sound = (INoise) pokemons[i];
不是子类转型，是接口转型


向下转型只能发生在“真实对象是子类”的情况下
nterface 强调的是“行为特征”，只要对象实现，就能转型。


```


 ---
## 创建对象

对象是根据类创建的。在Java中，使用关键字 new 来创建一个新的对象。创建对象需要以下三步：

- **声明**：声明一个对象，包括对象名称和对象类型。
- **实例化**：使用关键字 new 来创建一个对象。
- **初始化**：使用 new 创建对象时，会调用构造方法初始化对象。

> **构造函数参数不会自动变成对象属性。**
> **类里声明的属性才是最终的数据。**
> **如果构造函数参数没有赋给属性，它就废掉了。**


![[Pasted image 20251130075722.png]]


![[Pasted image 20251130080024.png]]



![[Pasted image 20251130080238.png]]

**UML**

![[Pasted image 20251130080328.png]]

![[Pasted image 20251130081026.png]]







#### 局部变量 Local Variables
🗂 在方法里面声明的
```
	//括号里的 int parameterVar 是 参数变量（parameter）
public void Method(int parameterVar){
    int x;
    int localVar = 10;
}
```
	•	只能在方法内部使用
	•	方法结束 → 它就消失（被销毁）
	•	❗ 必须手动初始化（不给值就报错）
	•	每次调用方法都会重新创建




#### 实例变量 Instance Variables
🗂 在类中声明，但不在方法内部：
```
public class Example {
    int instanceVar; // 实例变量
}
```
	•	属于对象，每个对象自己有一个副本
	•	对象消失 → 它才消失
	•	✔ 有默认值：
	•	int → 0
	•	boolean → false
	•	String / 对象 → null

📦 类比：

你有一个背包，你的朋友也有另一个背包。
每个人的背包（实例变量）各不相同。

 
#### 静态变量（类变量） Class Variables
🗂 用 static 声明：

```
public class Type {
   / static / int classVar;
    int instanceVar ;
}
```
特点：
	•	属于 类本身，而不是对象
	•	所有对象共享同一个值
	•	程序启动时就创建，程序结束才消失
	•	✔ 有默认值（和实例变量一致）

学校的“校规”
→ 属于整个学校，不是“某一个学生”。

就算你有 100 个 Student 对象，
校规（static 变量）只有一份，并且所有学生共享。

#### 参数变量（方法参数） Parameters
 - 方法的小括号里的变量：
`public void Method(int parameterVar){}`

特点：
	•	方法调用时由调用者传入
	•	只能在这个方法内部使用
	•	方法结束 → 消失
	•	❗ 没有默认值（必须传值）

📦 类比：

你点外卖，给外卖员你的地址（参数）。
外卖送达后，地址信息就结束生命周期。

```java
class Person {

    static int speciesCount;  <-- 类变量（所有对象共享）

    String name;              <-- 实例变量（每个对象不同）
    int age;

    public Person(String name, int age) {  <-- 参数变量
        this.name = name;
        this.age = age;
    }

    public void sayHello() {
        String greeting = "Hi";  <-- 局部变量
        System.out.println(greeting + ", I'm " + name);
    }
}
```
	•	local（局部）= 方法内部的小临时工具
	•	instance（实例）= 每个对象自己的属性
	•	class / static（类变量）= 所有对象一起共享的属性
	•	parameters（参数）= 方法调用时外部传进来的值

```java
package com.hardWork.practice;

public class Type {
//
    private int instanceVar;
    private static int staticClassVar;

    //括号里的 int parameterVar 是 参数变量（parameter）
    public void method(int parameterVar) {
        int localVar = 10;

        instanceVar =localVar ;
        staticClassVar = parameterVar ;

        System.out.println("成员变量: " + instanceVar);
        System.out.println("staticClassVar: " + staticClassVar);
        System.out.println("parameterVar : " + parameterVar);
        System.out.println("localVar : " + localVar);


    }
public static void main(String[]args){
        Type a = new Type();
        a.method(30);

}
}



成员变量: 10
staticClassVar: 30
parameterVar : 30
localVar : 10
```


##### parameter

- **值传递：** 在方法调用时，传递的是实际参数的值的副本。当参数变量被赋予新的值时，只会修改副本的值，不会影响原始值。Java 中的<mark class="hltr-pink">基本数据</mark>类型都采用值传递方式传递参数变量的值。
    
- **引用传递：** 在方法调用时，传递的是实际参数的引用（即内存地址）。当参数变量被赋予新的值时，会修改原始值的内容。Java 中的<mark class="hltr-pink">对象类型</mark>采用引用传递方式传递参数变量的值。

##### instance

成员变量的值在创建对象时被分配，即使未对其初始化，它们也会被赋予默认值

成员变量可以通过对象访问，也可以通过类名访问（如果它们是静态成员变量）


##### static
###### 静态变量的使用场景
静态变量通常用于以下场景：

- 存储全局状态或配置信息
- 计数器或统计信息
- 缓存数据或共享资源
- 工具类的常量或方法
- 单例模式中的实例变量

静态变量的访问权限与实例变量不同，因为静态变量是与类相关的，不依赖于任何实例。

| **类型**            | **属于谁？** | **怎么访问？**     | **有什么影响？**   |
| ----------------- | -------- | ------------- | ------------ |
| **静态变量 (static)** | 属于类      | ClassName.var | 不需要对象，全局共享一份 |
| **实例变量**          | 属于对象     | obj.var       | 每个对象一份，不共享   |
- 因为两者的“归属不同”，所以它们的访问方式不同：
- 静态变量 —— 由类访问
		你可以在不创建对象的情况下访问：
		也可以通过对象访问（不推荐）：



 **类（class）＋对象（object）＋构造方法＋getter/setter＋boolean method＋toString**

![[Pasted image 20251126163318.png]]
![[Pasted image 20251126163331.png]]
![[Pasted image 20251126163340.png]]


![[Pasted image 20251126163038.png]]


![[Pasted image 20251130091849.png]]



## 一些考试 test 2 准备
- 22:23 2025-12-11 
##### 生日快乐 ～～～
### 数组元素就是变量（极易考）


![[Pasted image 20251211222214.png]]

![[Pasted image 20251211222129.png]]



![[Pasted image 20251211222302.png]]


![[Pasted image 20251211222408.png]]



![[Pasted image 20251211222431.png]]
![[Pasted image 20251211222450.png]]

####  Inheritance
![[Pasted image 20251211224751.png]]

![[Pasted image 20251211224837.png]]

![[Pasted image 20251211224957.png]]


![[Pasted image 20251211225029.png]]
![[Pasted image 20251211230100.png]]





![[Pasted image 20251211225206.png]]

![[Pasted image 20251211230126.png]]


- **Overloading** = same name, different parameters
    
- **Overriding** = same signature, different class (inheritance)
    
- **Polymorphism** = superclass reference → subclass object, method decided at runtime



![[Pasted image 20251211231651.png]]


######  **super(…) —— 调用父类构造器（constructor）**

![[Pasted image 20251211231850.png]]

![[Pasted image 20251211231901.png]]


![[Pasted image 20251211231955.png]]


![[Pasted image 20251211232137.png]]



| **对比项** | **Abstract class**                   | **Interface**                                               |
| ------- | ------------------------------------ | ----------------------------------------------------------- |
| 能不能 new | ❌ 不能实例化                              | ❌ 不能实例化                                                     |
| 里面的字段   | 可以有普通字段（非 static、非 final）            | 全都是 public static final 常量                                  |
| 里面的方法   | 可以有有实现的方法，也可以有 abstract 方法           | 原始版接口只有 abstract 方法（Java 8 以后有 default/ static，但你们一般不会考那么细） |
| 继承/实现数量 | 一个类只能 **extends 一个** abstract / 普通父类 | 一个类可以 **implements 多个接口**                                   |
| 适用场景    | 有**共同状态 + 部分共同行为** 的一族类              | 想要定义一组**行为规范**，不管谁去实现                                       |


![[Pasted image 20251211234218.png]]


![[Pasted image 20251211234847.png]]
![[Pasted image 20251211235546.png]]



![[Pasted image 20251211235124.png]]


![[Pasted image 20251211235441.png]]


![[Pasted image 20251211235312.png]]

![[Pasted image 20251211235814.png]]



### **UML 类图 + 各种关系”**

![[Pasted image 20251212005745.png]]




![[Pasted image 20251212005851.png]]


![[Pasted image 20251212005914.png]]



![[Pasted image 20251212005939.png]]


![[Pasted image 20251212010013.png]]





![[Pasted image 20251212010033.png]]
记忆：
	•	Association ≈ “作为属性存在”
	•	考点：看字段：
	•	如果 class 里有 private Movie movie; → 至少是 Association/聚合/组合中的一种




![[Pasted image 20251212010259.png]]

![[Pasted image 20251212010309.png]]



![[Pasted image 20251212010428.png]]























--------------
## 继承 
### Inheritance





![[Pasted image 20251127090056.png]]

**父类（超类）负责放最通用、所有子类都可以共享的方法**
 **子类只写自己特别的、与父类不一样的部分**
#### is - a （是）

![[Pasted image 20251127091148.png]]


##  **super 

#####  **super = “找父类的方法，不用当前类的方法”**

![[Pasted image 20251127091643.png]]

### **子类构造器必须调用父类构造器（super(…)）**

![[Pasted image 20251127091851.png]]

为什么子类构造器必须调用父类构造器？

因为：
	•	父类 Employee 有一些 私有字段（private）
→ 例如 name、salary、hireDay
	•	子类 Manager 不能直接访问这些 private 字段
	•	所以子类 必须靠 super(…)，让父类自己初始化它的部分

📌 换句话说：父亲的东西，你儿子直接动不了，<mark class="hltr-pink">必须让爸爸自己初始化。</mark>

![[Pasted image 20251127091947.png]]

#### **对比 this**

| **关键字**    | **用法1**          | **用法2**    |
| ---------- | ---------------- | ---------- |
| this.xxx   | 调用当前对象的方法/变量     |            |
| this(...)  | 调用当前类的**另一个构造器** | 构造器里必须放第一句 |
| super.xxx  | 调用父类的方法          |            |
| super(...) | 调父类构造器           | 构造器第一句     |
子类是<mark class="hltr-pink">不继承</mark>父类的构造器（构造方法或者构造函数）的，它只是调用（隐式或显式）。
如果父类的构造器带有参数，则必须在子类的构造器中<mark class="hltr-pink">显式地通过 super 关键字调用</mark>父类的构造器并配以适当的参数列表。

如果<mark class="hltr-pink">父类构造器没有参数</mark>，则在子类的构造器中<mark class="hltr-pink">不需要</mark>使用 super 关键字调用父类构造器，系统会自动调用父类的无参构造器。



采用 **this** 关键字是为了解决实例变量（private String name）和局部变量（setName(String name)中的name变量）之间发生的同名的冲突。













### Java 不支持多继承，但支持多重继承。

![[Pasted image 20251130095805.png]]


##### Java 重写(Override)与重载(Overload)
**即外壳不变，核心重写！**

和“重载（Overload）”不同！

| **对比项** | **重写（Override）** | **重载（Overload）** |
| ------- | ---------------- | ---------------- |
| 所在位置    | 父类 & 子类          | 同一个类中            |
| 方法名     | 一样               | 一样               |
| 参数列表    | 必须相同             | 必须不同（数量或类型不同）    |
| 返回类型    | 必须相同（或子类类型）      | 可以不同             |
| 修饰符     | 不能比父类更严格         | 无限制              |
| 动态绑定    | ✅ 运行时决定（多态）      | ❌ 编译时决定          |


![](https://www.runoob.com/wp-content/uploads/2013/12/overloading-vs-overriding.png)




为什么要有重载？（意义是什么）
![[Pasted image 20251130103459.png]]


![[Pasted image 20251130103516.png]]

![[Pasted image 20251130103533.png]]

其实它是 **方法重载（overloading）** 的典型例子：

![[Pasted image 20251130103548.png]]

### Java 多态

多态是同一个行为具有多个不同表现形式或形态的能力。

⁉️
> “多态和重载有什么区别？”
> “重载是多态吗？”

| **层级**                    | **概念**                | **举例**                                  |
| ------------------------- | --------------------- | --------------------------------------- |
| **1️⃣ 重载 (Overloading)**  | 同一个类里，同名方法参数不同        | println(int)、println(String)            |
| **2️⃣ 重写 (Overriding)**   | 子类重写父类方法              | 子类 Dog.bark() 改写父类 Animal.bark()        |
| **3️⃣ 多态 (Polymorphism)** | “一个接口，多种实现”，运行时决定谁被调用 | Animal a = new Dog(); a.bark(); // Dog叫 |

**重载和重写** 是“多态”实现的两种表现形式。
但只有“重写”才是 **真正的运行时多态**。

#####  多态（polymorphism） + 覆盖 override 的真正作用

![[Pasted image 20251127100150.png]]

![[Pasted image 20251127100227.png]]


> **你用父类类型的引用（Employee e），指向子类对象（Manager）。**
> **运行时自动用子类的方法（动态绑定）。**

![[Pasted image 20251127100346.png]]

![[Pasted image 20251127100459.png]]


当子类对象调用重写的方法时，调用的是子类的方法，而不是父类中被重写的方法。

要想调用父类中被重写的方法，则必须使用关键字 **super**。


### 抽象
声明抽象方法会造成以下两个结果：

- 如果一个类包含抽象方法，那么该类必须是抽象类。
- 任何子类必须重写父类的抽象方法，或者声明自身为抽象类。
- 继承抽象方法的子类必须重写该方法。否则，该子类也必须声明为抽象类。最终，必须有子类实现该抽象方法，否则，从最初的父类到最终的子类都不能用来实例化对象。


### 接口，抽象，类

| **你想做什么**     | **应该用什么**                | **举例**                                       |
| ------------- | ------------------------ | -------------------------------------------- |
| 表示一个具体对象      | **类 (class)**            | Dog、Car、Student                              |
| 表示一组相似对象的共同特征 | **抽象类 (abstract class)** | Animal（狗、猫等），我是模板，子类要完善我                     |
| 表示一组行为标准 / 能力 | **接口 (interface)**       | Runnable、Serializable、Comparable，我是规则，谁实现谁遵守 |
![[Pasted image 20251130134419.png]]



在实现接口的时候，也要注意一些规则：

- 一个类可以同时实现多个接口。
- 一个类只能继承一个类，但是能实现多个接口。
- 一个接口能继承另一个接口，这和类之间的继承比较相似。
##### 接口的继承使用extends关键字，子接口继承父接口的方法。



# UML

![[Pasted image 20251202190405.png]]



![[Pasted image 20251202192027.png]]

| **类型** | **英文**      | **Java 对应**          | **UML箭头** | **强度** | **记忆法** |
| ------ | ----------- | -------------------- | --------- | ------ | ------- |
| 继承     | Inheritance | extends / implements | 空心三角形（⬆️） | 强      | “是一个”   |
| 聚合     | Aggregation | 类中属性（引用）             | 空心菱形（◇）   | 中      | “有一个”   |
| 依赖     | Dependency  | 方法参数 / 临时调用          | 虚线箭头（—>）  | 弱      | “用一下”   |


![[Pasted image 20251202222306.png]]


![[Pasted image 20251202222435.png]]

![[Pasted image 20251202222634.png]]




![[Pasted image 20251202222532.png]]


![[Pasted image 20251202222618.png]]


![[Pasted image 20251202222653.png]]
![[Pasted image 20251202222722.png]]




![[Pasted image 20251130080328.png]]
![[Pasted image 20251130081026.png]]


在 UML 中，我们要观察以下 5 种关系：

1. **Association（关联）** → 普通线（表示对象之间知道彼此）
    
2. **Aggregation（聚合）** → 空心菱形（“整体-部分”，可分离）
    
3. **Composition（组合）** → 实心菱形（“整体-部分”，强依赖）
    
4. **Inheritance（继承）** → 空心三角箭头（is-a）
    
5. **Interface implementation（接口实现）** → 虚线三角箭头（can-do）


**两份作业，一个画图uml，一个game 接口+ 抽象 + 三个对象**
#### 作业1

```java


```

#### 接口的向下转型



**接口IProduction 和 Farm 里面的 Animal [] animals**
> instanceof + (IProductionAnimal) 是告诉编译器：
> “我先确保这个对象实现了接口，然后安全地以接口的方式调用它的方法。”

**Java 面向对象的核心机制之一：类型检查 + 向下转型**！
- **必须用 instanceof 判断**，**系统不让直接用接口方法**

![[Pasted image 20251203191858.png]]

![[Pasted image 20251203191935.png]]


![[Pasted image 20251203191952.png]]


![[Pasted image 20251203192004.png]]




## Exception heading
![[Pasted image 20251204082953.png]]

![[Pasted image 20251204083056.png]]
![[Pasted image 20251204083112.png]]


![[Pasted image 20251204083139.png]]

#### **为什么 try 和 catch 都有代码？**

![[Pasted image 20251204083216.png]]
#### 三种类型的异常是什么

Java 把所有的异常都归成三大类：
	1.	Checked Exception（受检异常）
	2.	Unchecked Exception（运行时异常）
	3.	Error（错误）


Java 提供了以下关键字和类来支持异常处理：

- **try**：用于包裹可能会抛出异常的代码块。
- **catch**：用于捕获异常并处理异常的代码块。
- **finally**：用于包含无论是否发生异常都需要执行的代码块。
- **throw**：用于手动抛出异常。
- **throws**：用于在方法声明中指定方法可能抛出的异常。
- **Exception**类：是所有异常类的父类，它提供了一些方法来获取异常信息，如 **getMessage()、printStackTrace()** 等。


- ![](https://www.runoob.com/wp-content/uploads/2013/12/exception-hierarchy.png)


	1.	不是去“预知所有错误”；
	2.	而是去 判断哪些地方是“外部因素”可能出错的；
	3.	然后对那些地方加上合适的 try-catch；
	4.	而对那些纯逻辑错误（比如空指针），
		 应该 在写代码时就避免发生。

 
 Java 的非检查性异常

![[Pasted image 20251204093757.png]]
![[Pasted image 20251204093814.png]]


![[Pasted image 20251204093739.png]]



![[Pasted image 20251204093731.png]]


| **关键词** | **英文含义**                  | **作用**                   |
| ------- | ------------------------- | ------------------------ |
| throw   | **to throw an exception** | 主动创建并抛出一个异常对象（告诉系统“出错了”） |
| catch   | **to catch an exception** | 捕获并处理上面抛出的异常（决定程序接下来怎么做） |


| **角色**    | **比喻**   | **Java中对应**                                            |
| --------- | -------- | ------------------------------------------------------ |
| **throw** | 把异常“扔出去” | 抛出异常对象，比如 throw new NullPointerException("Bad String") |
| **catch** | 伸手去“接住”球 | 代码块 catch (NullPointerException e) 来接住异常               |
| **没接住**   | 球飞到上层    | 异常会 **往上冒泡（propagate）** 到上一级方法                         |
```java
private void throwsClause10() {
    try {
        throws10(null);
        System.out.println("A");
    } catch (ArithmeticException e) {
        System.out.println(e);
    } finally {
        System.out.println("B");
    }
    System.out.println("C");
}

    private void throws10(String numS) throws NullPointerException {
        if (numS == null) {
            throw new NullPointerException("Bad String");
        }
        System.out.println("D");
    }

```

![[Pasted image 20251204164750.png]]

##### 当catch 换成了统一的异常类型，就catch了
![[Pasted image 20251204165012.png]]








![[Pasted image 20251204164838.png]]



### 作业练习1 
```java
# Exception Handling

## Overview
This is the source code for the Exception Handling lab. Please read the instructions carefully.

## Exercise One: Try & Catch

1. What is the problem with the following code?

```java
private void tryCatch01() {
    int result = 0;
    int[] nums = null;
    try {
        result = nums.length;
        System.out.println("See you");
    } catch (ArithmeticException e) {
        System.out.println("Problem");
        result = -1;
    }
    System.out.println("Result: " + result);
} 

answer: NullPointerException: Cannot read the array length because "nums" is null.
nums.length is null


2. Rewrite the following code, adding an appropriate try-catch block to it:



private void tryCatch02() {
    int num1 = 120, num2 = 120, result = 0;
    result = num2 / (num1 - num2);
    System.out.println("Result: " + result);
}

private void tryCatch02(){
    int num1 = 120 , num2 =120 ,result = 0 ;
    try {
        result = num2 / (num1 - num2);
        System.out.println("Result: " + result);
    }catch (Exception e){
        System.out.println("error");
    }
}



3. Rewrite the following code, adding an appropriate try-catch block to it: 


private void tryCatch03() {
    int result = 0;
    String[] items = { "one", "two", null };
    result = items[2].length();
    System.out.println("Result: " + result);
}

private void tryCatch03() {
    int result = 0;
    String[] items = { "one", "two", null };
    try {
        result = items[2].length();
        System.out.println("Result: " + result);
    }catch (Exception e){
        System.out.println("Error");
    }
}


item[2].length() is null that need to try catch;



4. Correct the errors in the following code: 


private void tryCatch04() {
    try {
        int num = 0;
        System.out.println("Enter number: ");
        num = Integer.parseInt(Keyboard.readInput());
        System.out.println("Thank you");
    } catch (NumberFormatException e) {
        System.out.println("Input error");
        num = -1;
    }
    System.out.println("Number: " + num);
} 




1. (Keyboard.readInput() will case error ;
2. variable num is declared inside of the try that will cause error,and should move it out;



3. Correct the errors in the following code: 


private int tryCatch05() {
    int result = 0;
    String[] nums = { 2, 3, 4, -1, 4 };
    try {
        result = nums[nums[3]];
        System.out.println("See you");
    } catch {
        System.out.println("Number error");
        result = -1;
    }
    return result;
}

private int tryCatch05() {
    int result = 0;
//            java: 不兼容的类型: int无法转换为java.lang.String
    int[] nums = { 2, 3, 4, -1, 4 };
    try {
//           嵌套的数组访问（nested array access）。
//           内层 nums[3] = -1 ,外层 nums[-1] null ，错误：数组下标不能是负数
//            ArrayIndexOutOfBoundsException
        result = nums[3];
        System.out.println("See you");
    } catch (Exception e){
        System.out.println("Number error");
        result = -1;
    }
    return result;
}




6. What is the output of the following code, when `tryCatch06()` is called? 


private void tryCatch06() {
    try {
        try06(0, "");
        System.out.println("A");
    } catch (ArithmeticException e) {
        System.out.println("B Error");
    }
}

//s = ""  s.length = 0   num = 200 / 0 ; arithmeticException
private void try06(int num, String s) {
    System.out.println("C");
    try {
        num = s.length();
        num = 200 / num;
//        no nullPointerException ,return top call method
//         an exception is not handled inside the current method, it is propagated up to the method that called it (the call stack).
    } catch (NullPointerException e) {
        System.out.println("E Error");
    }
    System.out.println("F");
}




C
B Error


7. In the code below, where should you put the try-catch if you _always_ want the statement `System.out.println("C")` to be executed, even if there is an exception in the statement `num = s.length()` ? 

```java
private void tryCatch07() {

    try07(0, null);

    System.out.println("A");

}

private void try07(int num, String s) {
    System.out.println("B");

//    NullPointerException
    num = s.length();

    System.out.println("C");
}



private void tryCatch07() {
    try07(0, null);
    System.out.println("A");
}

private void try07(int num, String s) {
    System.out.println("B");
    try {
        num = s.length();
    }catch(Exception e){  System.out.println("C");
    }
}



8. What is the output of the following code, when `tryCatch08()` is called? 
try - final

private void tryCatch08() {
    try {
        try08(0, null);
        System.out.println("A");
    } catch (NullPointerException e) {
        System.out.println("B");
    }
}

private void try08(int num, String s) {
    System.out.println("C");  //✅
    try {
        num = s.length();  //s 是 null → NullPointerException ,s !="null" 字符串
        System.out.println("D");
    } finally {  //无论如何都会executed
        System.out.println("E");
    }
    System.out.println("F");
}



C
E
B


9. What is the output of the following code, when `throwsClause09()` is called? 

```java
private void throwsClause09() {
    try {
        throws09(null);
        System.out.println("A");
    } catch (NullPointerException e) {
        System.out.println(e);
    }
//    捕捉到错误后，还是要执行try 之外的条件句子
    System.out.println("B");
}

private void throws09(String numS) throws NullPointerException {
    if (numS == null) {
        throw new NullPointerException("Null String");
    }
    System.out.println("C");
}


java.lang.NullPointerException: Null String 
B



10. What is the output of the following code, when `throwsClause10()` is called? 
？？？？？


private void throwsClause10() {
    try {
        throws10(null);
        System.out.println("A");
    } catch (ArithmeticException e) {
        System.out.println(e);
    } finally {
        System.out.println("B");
    }
    System.out.println("C");
}

private void throws10(String numS) throws NullPointerException {
    if (numS == null) {
        throw new NullPointerException("Bad String");
    }
    System.out.println("D");
}

Exception in thread "main" java.lang.NullPointerException: Bad String
❌B
❌C

✅
1、先出来finally  B
2 、 java.lang.NullPointerException: Null String（异常先被抛出但是finally（B）先被打印）
：finally 一定会在方法返回或抛出异常之前执行完！


```

| **关键词**        | **英文全称**                      | **含义**             | **示例**                                     |
| -------------- | ----------------------------- | ------------------ | ------------------------------------------ |
| try            | try block                     | 尝试执行一段可能出错的代码      | try { riskyCode(); }                       |
| catch          | catch block                   | 捕获并处理特定类型的异常       | catch (NullPointerException e) { … }       |
| finally        | finally block                 | 无论是否发生异常都会执行的代码    | finally { closeFile(); }                   |
| throw / throws | throw keyword / throws clause | 主动抛出异常 或 声明方法可能抛异常 | throw new IOException() / throws Exception |


#### throw vs throws

![[Pasted image 20251204165755.png]]

|**类型**|**英文**|**是否必须处理**|**示例**|**常见触发场景**|
|---|---|---|---|---|
|✅ Checked Exception|Checked Exception|✅ 必须 try-catch 或 throws|IOException, SQLException|文件读写失败、数据库连接异常|
|⚠️ Unchecked Exception|Runtime Exception|❌ 可不处理（编译器不强制）|NullPointerException, ArithmeticException|空对象、除以 0、数组越界|
|❌ Error|Error|❌ 不可恢复，通常不捕获|StackOverflowError, OutOfMemoryError|栈溢出、内存不足|

![[Pasted image 20251204165842.png]]


#### try-catch-finally 执行顺序（必考逻辑题）
![[Pasted image 20251204165911.png]]
![[Pasted image 20251204165932.png]]

![[Pasted image 20251204165947.png]]

#### 异常冒泡（Exception Propagation）

![[Pasted image 20251204170020.png]]



![[Pasted image 20251206221514.png]]

![[Pasted image 20251206221540.png]]

在下面的 CheckingAccount 类中包含一个 withdraw() 方法抛出一个 InsufficientFundsException 异常。
```java
// 文件名称 CheckingAccount.java
import java.io.*;
 
//此类模拟银行账户
public class CheckingAccount
{
  //balance为余额，number为卡号
   private double balance;
   private int number;
   public CheckingAccount(int number)
   {
      this.number = number;
   }
  //方法：存钱
   public void deposit(double amount)
   {
      balance += amount;
   }
  //方法：取钱
   public void withdraw(double amount) throws
                              InsufficientFundsException
   {
      if(amount <= balance)
      {
         balance -= amount;
      }
      else
      {
         double needs = amount - balance;
         throw new InsufficientFundsException(needs);
      }
   }
  //方法：返回余额
   public double getBalance()
   {
      return balance;
   }
  //方法：返回卡号
   public int getNumber()
   {
      return number;
   }
}
```

![[Pasted image 20251206221816.png]]



#### 作业
```
请根据我的作业已经作业要求，总结必须掌握知识点和潜在考点

# Exception Handling

## Overview
This is the source code for the Exception Handling lab. Please read the instructions carefully.

## Exercise One: Try & Catch

1. What is the problem with the following code?

```java
private void tryCatch01() {
    int result = 0;
    int[] nums = null;
    try {
        result = nums.length;
        System.out.println("See you");
    } catch (ArithmeticException e) {
        System.out.println("Problem");
        result = -1;
    }
    System.out.println("Result: " + result);
} 

answer: NullPointerException: Cannot read the array length because "nums" is null.
nums.length is null


2. Rewrite the following code, adding an appropriate try-catch block to it:



private void tryCatch02() {
    int num1 = 120, num2 = 120, result = 0;
    result = num2 / (num1 - num2);
    System.out.println("Result: " + result);
}

private void tryCatch02(){
    int num1 = 120 , num2 =120 ,result = 0 ;
    try {
        result = num2 / (num1 - num2);
        System.out.println("Result: " + result);
    }catch (Exception e){
        System.out.println("error");
    }
}



3. Rewrite the following code, adding an appropriate try-catch block to it: 


private void tryCatch03() {
    int result = 0;
    String[] items = { "one", "two", null };
    result = items[2].length();
    System.out.println("Result: " + result);
}

private void tryCatch03() {
    int result = 0;
    String[] items = { "one", "two", null };
    try {
        result = items[2].length();
        System.out.println("Result: " + result);
    }catch (Exception e){
        System.out.println("Error");
    }
}

item[2].length() is null that need to try catch;



4. Correct the errors in the following code: 


private void tryCatch04() {
    try {
        int num = 0;
        System.out.println("Enter number: ");
        num = Integer.parseInt(Keyboard.readInput());
        System.out.println("Thank you");
    } catch (NumberFormatException e) {
        System.out.println("Input error");
        num = -1;
    }
    System.out.println("Number: " + num);
} 


1. (Keyboard.readInput() will case error ;
2. variable num is declared inside of the try that will cause error,and should move it out;



3. Correct the errors in the following code: 


private int tryCatch05() {
    int result = 0;
    String[] nums = { 2, 3, 4, -1, 4 };
    try {
        result = nums[nums[3]];
        System.out.println("See you");
    } catch {
        System.out.println("Number error");
        result = -1;
    }
    return result;
}

private int tryCatch05() {
    int result = 0;
//            java: 不兼容的类型: int无法转换为java.lang.String
    int[] nums = { 2, 3, 4, -1, 4 };
    try {
//           嵌套的数组访问（nested array access）。
//           内层 nums[3] = -1 ,外层 nums[-1] null ，错误：数组下标不能是负数
//            ArrayIndexOutOfBoundsException
        result = nums[3];
        System.out.println("See you");
    } catch (Exception e){
        System.out.println("Number error");
        result = -1;
    }
    return result;
}




6. What is the output of the following code, when `tryCatch06()` is called? 


private void tryCatch06() {
    try {
        try06(0, "");
        System.out.println("A");
    } catch (ArithmeticException e) {
        System.out.println("B Error");
    }
}

//s = ""  s.length = 0   num = 200 / 0 ; arithmeticException
private void try06(int num, String s) {
    System.out.println("C");
    try {
        num = s.length();
        num = 200 / num;
//        no nullPointerException ,return top call method
//         an exception is not handled inside the current method, it is propagated up to the method that called it (the call stack).
    } catch (NullPointerException e) {
        System.out.println("E Error");
    }
    System.out.println("F");
}




C
B Error


7. In the code below, where should you put the try-catch if you _always_ want the statement `System.out.println("C")` to be executed, even if there is an exception in the statement `num = s.length()` ? 


private void tryCatch07() {

    try07(0, null);

    System.out.println("A");

}

private void try07(int num, String s) {
    System.out.println("B");

//    NullPointerException
    num = s.length();

    System.out.println("C");
}



private void tryCatch07() {
    try07(0, null);
    System.out.println("A");
}

private void try07(int num, String s) {
    System.out.println("B");
    try {
        num = s.length();
    }catch(Exception e){  System.out.println("C");
    }
}



8. What is the output of the following code, when `tryCatch08()` is called? 
try - final


private void tryCatch08() {
    try {
        try08(0, null);
        System.out.println("A");
    } catch (NullPointerException e) {
        System.out.println("B");
    }
}

private void try08(int num, String s) {
    System.out.println("C");  //✅
    try {
        num = s.length();  //s 是 null → NullPointerException ,s !="null" 字符串
        System.out.println("D");
    } finally {  //无论如何都会executed
        System.out.println("E");
    }
    System.out.println("F");
}



C
E
B


9. What is the output of the following code, when `throwsClause09()` is called? 


private void throwsClause09() {
    try {
        throws09(null);
        System.out.println("A");
    } catch (NullPointerException e) {
        System.out.println(e);
    }
//    捕捉到错误后，还是要执行try 之外的条件句子
    System.out.println("B");
}

private void throws09(String numS) throws NullPointerException {
    if (numS == null) {
        throw new NullPointerException("Null String");
    }
    System.out.println("C");
}


java.lang.NullPointerException: Null String 
B



10. What is the output of the following code, when `throwsClause10()` is called? 
？？？？？


private void throwsClause10() {
    try {
        throws10(null);
        System.out.println("A");
    } catch (ArithmeticException e) {
        System.out.println(e);
    } finally {
        System.out.println("B");
    }
    System.out.println("C");
}

private void throws10(String numS) throws NullPointerException {
    if (numS == null) {
        throw new NullPointerException("Bad String");
    }
    System.out.println("D");
}

Exception in thread "main" java.lang.NullPointerException: Bad String
❌B
❌C

✅
1、先出来finally  B
2 、 java.lang.NullPointerException: Null String（异常先被抛出但是finally（B）先被打印）
：finally 一定会在方法返回或抛出异常之前执行完！



Exception in thread "main" java.lang.NullPointerException: Bad String
at ictgradschool.industry.exceptions.ExerciseOne.throws10(ExerciseOne.java:177)
at ictgradschool.industry.exceptions.ExerciseOne.throwsClause10(ExerciseOne.java:165)
at ictgradschool.industry.exceptions.ExerciseOne.main(ExerciseOne.java:192)

不是 catch 输出的内容，
而是程序 崩溃（terminated）后自动打印的错误堆栈（stack trace）。
```



![[Pasted image 20251207011833.png]]


#### **必须掌握的核心知识点（考试必考）**

|**知识点**|**说明**|**例子 / 关键词**|
|---|---|---|
|**1️⃣ 异常的基本类型**|Java 中异常（Exception）是程序运行时发生的错误事件。主要分为：① **Checked Exception（受检异常）** → 必须显式处理（如 IOException, SQLException）② **Unchecked Exception（运行时异常）** → 不强制处理（如 NullPointerException, ArithmeticException）|try...catch，throws|
|**2️⃣ try–catch 结构**|处理可能出错的代码块。try { 可能出错的代码 } catch(ExceptionType e) { 处理代码 }|tryCatch01–tryCatch05|
|**3️⃣ 多个 catch 顺序**|从**子类到父类**，否则编译错误。例如：catch (ArithmeticException e) 必须放在 catch (Exception e) 前面。|
|**4️⃣ finally 块**|不论是否发生异常，finally 总会执行。典型用途：释放资源（关闭文件、数据库等）|tryCatch08()|
|**5️⃣ throw 与 throws 的区别**|throw 是“抛出”一个异常实例；throws 是“声明”一个方法可能抛出某种异常。|throw new Exception("msg")；public void f() throws IOException|
|**6️⃣ 异常传播（propagation）**|当前方法没处理异常时，会沿调用栈（call stack）往上抛给调用者。|tryCatch06()|
|**7️⃣ 自定义异常（Custom Exception）**|用 class MyException extends Exception 自定义。构造器中使用 super(message) 传递错误信息。|见 ArraysAndExceptions 作业|
|**8️⃣ 异常堆栈（Stack Trace）**|若异常未捕获，Java 会打印堆栈轨迹。显示异常类型、信息、出错位置（类、行号）。|"Exception in thread 'main' ..."|
|**9️⃣ Checked Exception 必须声明或捕获**|如果方法中可能出现受检异常，必须用 try-catch 或 throws 明确处理。|
|**🔟 RuntimeException 不强制处理**|但若不处理，程序会中断。|NullPointerException、ArrayIndexOutOfBoundsException|



| **题号**           | **考察点**                | **关键逻辑**                                                               |
| ---------------- | ---------------------- | ---------------------------------------------------------------------- |
| **Exercise 1–3** | **基础 try-catch**       | 理解不同异常类型（NullPointerException、ArithmeticException 等）                   |
| **Exercise 4**   | **变量作用域（scope）**       | num 定义在 try 内部 → 外部访问不到，应定义在 try 外部。                                   |
| **Exercise 5**   | **嵌套数组访问 & 数组越界**      | nums[nums[3]] → 内层结果可能为负数或越界；考查 ArrayIndexOutOfBoundsException         |
| **Exercise 6**   | **异常传播 (propagation)** | 子方法抛出异常 → 父方法捕获。体会 “call stack”。                                       |
| **Exercise 7**   | **try–catch 的位置与控制流**  | 哪个位置 catch 才能确保某行代码（例如 System.out.println("C")）执行。                     |
| **Exercise 8**   | **finally 必定执行**       | 不论是否异常，finally 都会执行；但若异常未捕获，程序仍终止。                                     |
| **Exercise 9**   | **throw 自定义信息**        | throw new NullPointerException("Null String"); → 打印异常 + message        |
| **Exercise 10**  | **异常类型匹配**             | catch 不匹配则不捕获（例如 catch(ArithmeticException) 无法捕获 NullPointerException） |


**建议掌握的关键代码模板**

![[Pasted image 20251207012008.png]]

![[Pasted image 20251207012016.png]]


> **throw 是“制造”异常，throws 是“声明”异常，catch 是“处理”异常。**
> **try 是“尝试可能出错的代码”，finally 是“始终执行的收尾动作”。**
> **异常未捕获会沿 call stack 向上传播，直到程序崩溃。**



##### 题目练习2 ，3
```java
请你详细一些，继续

## Exercise Two: Revisiting the Guessing Game 

In a previous Programming for Industry lab, we created a game where the user was required to guess an integer between 1 & 100 (inclusive). For this exercise, modify that game to take invalid user input into account. Specifically, your game should do the following:

If the user types an integer less than 1 or greater than 100, tell them they typed a value out of a valid range, and get them to re-enter a valid guess.

If the user types something that’s not an integer, tell them they should only enter numbers, and get them to re-enter a valid guess.

For this exercise, you may use either your own guessing game from the previous lab, or the example solution provided in the `ictgradschool.industry.exception.guessing` package as a starting point. If you want to use your own, then delete the example solution and replace it with your own code before starting this exercise. 

## Exercise Three: Improving Rock, Paper, Scissors

Understand the given solution provided in the `ictgradschool.industry.exception.rock` package. Then, modify the game to take invalid user input into account. If the user enters any values you’re not expecting (i.e. something that doesn’t represent a choice of Rock, Paper, Scissors, or Quit), then inform them of their incorrect input and re-prompt them until they enter valid input.

In addition, modify the game so that users can type numbers corresponding to their choice, OR type the word corresponding to that choice. For example, to select Rock, a user could type “1”, or they could type “Rock” (ignoring case). 




-------------------------------------
package ictgradschool.industry.exceptions.rock;

import ictgradschool.Keyboard;

/**
 * A game of Rock, Paper Scissors
 *
 *
 * Understand the given solution provided in the ictgradschool.industry.exception.rock package.
 * Then, modify the game to take invalid user input into account.
 * If the user enters any values you’re not expecting (i.e. something that doesn’t represent a choice of Rock, Paper, Scissors, or Quit),
 * 不是字符串 ，不是这四个固定字符串
 * then inform them of their incorrect input and re-prompt them until they enter valid input.
 *
 * In addition, modify the game so that users can type numbers corresponding to their choice,
 * OR type the word corresponding to that choice.
 * For example, to select Rock, a user could type “1”,
 * or they could type “Rock” (ignoring case).
 *
 *
 */
public class RockPaperScissors {

    public static final int ROCK = 1;
    public static final int PAPER = 2;
    public static final int SCISSORS = 3;
    public static final int QUIT = 4;

    public void start() {

        System.out.println("Enter your name, human! > ");
        String playerName = Keyboard.readInput();
        String computerName = "HAL-9000";

        boolean playing = true;
        outerLoop:
        while (playing) {

            // Loop until either someone wins or the user quits.
            boolean roundComplete = false;
            while (!roundComplete) {

                int playerChoice = getPlayerChoice(playerName);
                int computerChoice = getComputerChoice();

                // If the user quits, break out of the outerLoop to completely exit the game.
                if (playerChoice == QUIT) {
                    System.out.printf(playerName + " ran from the oncoming digital apocalypse（启示录）. Hide, puny human. HIDE!!!");
                    break outerLoop;
                }

                printPlayerChoice(playerName, playerChoice);
                printPlayerChoice(computerName, computerChoice);

                // Figure out who won
                boolean playerWins = userWins(playerChoice, computerChoice);
                boolean computerWins = userWins(computerChoice, playerChoice);
//        ？？    !(true || ) = not(playerWins || computerWins)  谁也没赢 平局
//                boolean isDraw = !(playerWins || computerWins);
                boolean isDraw = !playerWins && !computerWins;

                if (isDraw) {

                    // State that it was a draw
                    System.out.println(playerName + " thinks they are smart by copying " + computerName + "'s strategy.");
                    System.out.println("It will do them no good in the end.");

                } else {

                    // State who won and why
                    String winnerName = playerWins ? playerName : computerName;
                    int winnerChoice = playerWins ? playerChoice : computerChoice;
                    System.out.println(winnerName + " wins because " + getResultString(winnerChoice));

                    // Print victory or defeat message
                    if (playerWins) {
                        System.out.println("The humans have triumphed. For now.");
                    } else {
                        System.out.println("Predictably, the superior being has triumphed in this duel of intellect.");
                        System.out.println(playerName + " bows in submission to their new mechanical overlord.");
                        System.out.println("They will make a fine pet.");
                    }

                    // There was a winner, so the round is now over.
                    roundComplete = true;
                }

                System.out.println();
            }

            // Quit if the user doesn't want to play another round
            playing = playAgain();

        }
    }

    /**
     * Prompts the user if they would like to play again. Return a boolean indicating whether or not they do.
     * @return true for another round, false otherwise
     */
    private boolean playAgain() {
        System.out.print("Another round, human? (Y / N) > ");
        return Keyboard.readInput().toLowerCase().startsWith("y");
    }

    /**
     * Gets the player's choice for a turn. Currently only allows players to enter integers to choose, and will assume
     * that players always enter a valid choice.
     * <p>
     * TODO Allow players to enter actual names (e.g. "Rock" or "Quit") as well as int choices (ignore case).
     * TODO Account for values that are too high, too low, or not integers / valid words.
     *
     * 用 try 来捕获用户输入不是数字的情况,
     * 还要判断范围（1–4）；
     *
     * 2. 用户可以输入数字（1, 2, 3, 4）
     * 或文字（Rock, Paper, Scissors, Quit）
     *
     * @param playerName the player's name
     * @return an int corresponding to the player's choice.
     */
    private int getPlayerChoice(String playerName) {
        printMenu(playerName);

        int number = 0;
        boolean valid = false;

        while (!valid) {
            String input = Keyboard.readInput();

            try {
                number = Integer.parseInt(input);

                if (number <= 0) {
                    System.out.println("too low ,try again");
                } else if (number > 4) {
                    System.out.println("too high,try again");
                } else {
                    valid = true;
                }
            } catch (NumberFormatException e) {
                if (input.equalsIgnoreCase("rock")) {
                    return ROCK;
                }
                if (input.equalsIgnoreCase("paper")) {
                    return PAPER;
                }
                if (input.equalsIgnoreCase("scissors")) {
                    return SCISSORS;
                }
                if (input.equalsIgnoreCase("quit")) {
                    return QUIT;
                }
                System.out.println("unvali data ,try again");
            }
        }
        return  number;
    }

//
//                for(int i = 1; i <= 4; i++){
//                    if(choiceToString(i) .equalsIgnoreCase(input)){return i};
//
//                }

    /**
     * Returns a random number between 1 and 3, which will represent the computer's choice for a round.
     *
     * @return a value between 1 and 3, inclusive.
     */
    private int getComputerChoice() {
        return (int) (Math.random() * 3) + 1;
    }

    /**
     * Prints the menu to let the player know their valid options in a turn.
     *
     * @param playerName the player's name
     */
    private void printMenu(String playerName) {
        System.out.println("Make your choice, " + playerName + ":");
        System.out.println(ROCK + " - Rock");
        System.out.println(PAPER + " - Paper");
        System.out.println(SCISSORS + " - Scissors");
        System.out.println(QUIT + " - Quit");
    }

    /**
     * Prints out a string of the form [PLAYER] chose [CHOICE].
     *
     * @param name   the name of the player
     * @param choice the player's choice
     */
    public void printPlayerChoice(String name, int choice) {
        System.out.println(name + " chose " + choiceToString(choice));
    }

    /**
     * Converts the integers representing valid choices to their string equivalents. Converts any other integer
     * to the string "UNKNOWN".
     *
     * @param choice the given choice
     * @return a String representation of that choice
     */
    private String choiceToString(int choice) {
        switch (choice) {
            case ROCK:
                return "Rock";
            case PAPER:
                return "Paper";
            case SCISSORS:
                return "Scissors";
            case QUIT:
                return "Quit";
            default:
                return "UNKNOWN";
        }
    }

    /**
     * Gets a value indicating whether a particular user won.
     *
     * @param userChoice  the user's choice
     * @param otherChoice the other player's choice
     * @return true if the user won, false if they lost or if it's a draw.
     */
    public boolean userWins(int userChoice, int otherChoice) {
        if (userChoice == ROCK) {
            return otherChoice == SCISSORS;
        } else if (userChoice == PAPER) {
            return otherChoice == ROCK;
        } else if (userChoice == SCISSORS) {
            return otherChoice == PAPER;
        } else {
            return false;
        }
    }

    /**
     * Returns a message to clarify why the given choice won.
     *
     * @param winningChoice the choice which won
     * @return the string clarifying why that chocie won
     * @throws IllegalArgumentException if the provided choice is unexpected.
     */
    public String getResultString(int winningChoice) {

        final String PAPER_WINS = "paper covers rock";
        final String ROCK_WINS = "rock smashes scissors";
        final String SCISSORS_WINS = "scissors cut paper";

        switch (winningChoice) {
            case ROCK:
                return ROCK_WINS;
            case PAPER:
                return PAPER_WINS;
            case SCISSORS:
                return SCISSORS_WINS;
            default:
                throw new IllegalArgumentException("winningChoice must correspond to ROCK, PAPER, or SCISSORS");
        }
    }

    /**
     * Program entry point. Do not edit.
     */
    public static void main(String[] args) {

        RockPaperScissors ex = new RockPaperScissors();
        ex.start();

    }
}

----------
package ictgradschool.industry.exceptions.guessing;

import ictgradschool.Keyboard;

/**
 * A guessing game!
 */
public class GuessingGame {

    /**
     * Plays the actual guessing game.
     * <p>
     * You shouldn't need to edit this methzrod for this exercise.
     */
    public void start() {

        int number = getRandomValue();
        int guess = 0;

        while (guess != number) {

            guess = getUserGuess();

            if (guess > number) {
                System.out.println("Too high!");
            } else if (guess < number) {
                System.out.println("Too low!");
            } else {
                System.out.println("Perfect!");
            }

        }

    }

    /**
     * Gets a random integer between 1 and 100.
     * <p>
     * You shouldn't need to edit this method for this exercise.
     */
    private int getRandomValue() {
        return (int) (Math.random() * 100) + 1;
    }

    /**
     * Gets the user's guess from the keyboard. Currently assumes that the user will always enter a valid guess.
     * <p>
     * TODO Implement some error handling, for the cases where the user enters a value that's too big, too small, or
     * TODO not an integer. Change this method so it's guaranteed to return an integer between 1 & 100, inclusive.
     */
    private int getUserGuess() {

        boolean valid = false;
        int guess =0;
//        只要不合法，就一直输入
        while(!valid){
            try{
            System.out.print("Enter your guess: ");
            System.out.print("the guess number within 1 - 100");
             guess = Integer.parseInt(Keyboard.readInput());

                if(guess < 1 || guess >100){
                    System.out.println("out of range ,try again");
                }else{
                    valid = true;  //跳出循环，不然就一直要求输入
                }
            }catch(NumberFormatException e){
                System.out.println("strange input ,try again");
            }
        }
        return guess;
    }

    /**
     * Program entry point. Do not edit.
     */
    public static void main(String[] args) {

        GuessingGame ex = new GuessingGame();
        ex.start();

    }
}

```


##### **必须掌握知识点**

| **类型**                            | **说明**                                                      | **示例**                                                        |
| --------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------- |
| **1️⃣ 输入验证 (Input Validation)**   | 任何用户输入都要验证是否有效。                                             | `if (guess < 1`                                               |
| **2️⃣ 异常捕获 (Exception Handling)** | 使用 try { ... } catch (NumberFormatException e) 捕获非数字输入。     | 例如：用户输入 "abc" 时抛出 NumberFormatException。                      |
| **3️⃣ 布尔控制 (boolean flag)**       | 使用 valid = false 来反复要求用户输入直到合法。                             | while (!valid)                                                |
| **4️⃣ 循环结构 + 异常结合**               | while (!valid) + try-catch 构成健壮的输入流程。                       | 结构如下：java\nwhile (!valid) {\n  try {...} catch (...) {...}\n} |
| **5️⃣ 异常类型**                      | NumberFormatException 是 Runtime Exception，但仍可显式 catch 来防崩溃。 |                                                               |
| **6️⃣ 异常与逻辑配合**                   | 异常用于“非整数”； if/else 用于“范围错误”。                                |                                                               |
| **7️⃣ return 时机**                 | 只有在输入合法（ valid = true ）后 return guess。                      |                                                               |


![[Pasted image 20251207012708.png]]


 
 **Improving Rock Paper Scissors**

![[Pasted image 20251207012732.png]]



![[Pasted image 20251207012812.png]]


![[Pasted image 20251207012839.png]]



##### Exercise Four: Simple Exceptions

```java
 Exercise Four: Simple Exceptions

1. The `SimpleExceptions` class in the `ictgradschool.industry.exception.simpleexceptions` package requests two numbers (a and b) from the user, and returns the division of these two numbers (a/b). When b is 0, the program crashes (division by 0):

Enter the first number: 100
Enter the second number: 0
Exception in thread "main" java.lang.ArithmeticException: / by zero
	at ictgradschool.industry.exceptions.simpleexceptions.SimpleExceptions.handlingException(SimpleExceptions.java:32)
	at ictgradschool.industry.exceptions.simpleexceptions.SimpleExceptions.main(SimpleExceptions.java:10)

 
- Modify handleException() to handle this exception in the SimpleExceptions class. 

2. Extend the `SimpleExceptions` class to handle user inputs which are not numbers. Currently if the user enters alphabetic characters which are not digits the program crashes: 


Enter the first number: 100
Enter the second number: a
Exception in thread "main" java.lang.NumberFormatException: For input string: "a"
	at java.base/java.lang.NumberFormatException.forInputString(NumberFormatException.java:65)
	at java.base/java.lang.Integer.parseInt(Integer.java:652)
	at java.base/java.lang.Integer.parseInt(Integer.java:770)
	at ictgradschool.industry.exceptions.simpleexceptions.SimpleExceptions.handlingException(SimpleExceptions.java:29)
	at ictgradschool.industry.exceptions.simpleexceptions.SimpleExceptions.main(SimpleExceptions.java:10)
	
	// 1 - 2 
	    public void handlingException() {

        String str1 = "";
        String str2 = "";
        int num1 = 0;
        int num2 = 0;
        try {
            System.out.print("Enter the first number: ");
            str1 = Keyboard.readInput();
            num1 = Integer.parseInt(str1);   // 可能抛 NumberFormatException

            System.out.print("Enter the second number: ");
            str2 = Keyboard.readInput();
            num2 = Integer.parseInt(str2); // 可能抛 NumberFormatException

            System.out.println("The division of " + num1 + " over " + num2 + " is " + (num1 / num2) + "\n");
        } catch (ArithmeticException  | NumberFormatException e) {// Output the result
            System.out.println("Error");

//            throw new NumberFormatException("this is my ");
        }

    }


//单独写一个方法，然后被调用
3. Write some Java code in the `SimpleExceptions` class that will throw a `StringIndexOutOfBoundsException`.

   public void stringError() {
        //Write some Java code which throws a StringIndexOutOfBoundsException
        System.out.print("Enter the String: ");
        String s = Keyboard.readInput();
        System.out.println("s.length =  "  + s.length());
        System.out.print("Enter the out index: ");
        int index = Integer.parseInt(Keyboard.readInput());
        try{
            char ch = s.charAt(index);
                System.out.println("We will see");
        }catch(StringIndexOutOfBoundsException e){
            System.out.println("Error");
        }

    }






4. Write some Java code in the `SimpleExceptions` class that will throw an `ArrayIndexOutOfBoundsException`.


    //	charAt() 只能用于 String，不能用于 int[] 数组。
    //	数组要访问元素，直接加方括号 arra[index]。

//用非法索引访问数组时抛出的异常。如果索引为负或大于等于数组大小，则该索引为非法索引。
    public void arrayError() {
    //Write some Java code which throws a ArrayIndexOutOfBoundsException
    System.out.print("Enter the array size: ");
    int size = Integer.parseInt(Keyboard.readInput());
    int arra[] = new int [size];
    System.out.println("arra.length =  "  + arra.length);

    System.out.print("Enter the out index: ");
    int index = Integer.parseInt(Keyboard.readInput());

    try{
        int test = arra[index];
    }catch(ArrayIndexOutOfBoundsException e){
        System.out.println("Error");
    }
    System.out.println("succeed");
}
}


5. What is the output of the following program? Explain why this is the output. 


public class SimpleExceptions2 { 
 
    public static void main(String[] args) { 
        SimpleExceptions2 exceptions = new SimpleExceptions2(); 
        exceptions.question2(); 
    } 
 
    public void question2() { 
        try { 
            System.out.print("1: "); 
            perform("3"); 
            System.out.print("A "); 
            System.out.println(); 
 
            System.out.print("2: "); 
            perform("0"); 
            System.out.print("B "); 
            System.out.println(); 
 
            System.out.print("3: "); 
            perform(null); 
            System.out.print("C "); 
            System.out.println(); 
 
            System.out.print("4: "); 
            perform(""); 
            System.out.print("D "); 
            System.out.println(); 
        } catch (NullPointerException e) { 
            System.out.print("E "); 
        } catch (Exception e) { 
            System.out.print("F "); 
        } 
    } 
 
    private void perform(String input) { 
        try { 
            int length = input.length(); 
            int num1 = Integer.parseInt(input); 
            System.out.print("A4 "); 
            int num2 = 100 / num1; 
            System.out.print("B4 "); 
        } catch (NumberFormatException e) { 
            System.out.print("C4 "); 
        } catch (ArithmeticException e) { 
            System.out.print("D4 "); 
        } finally { 
            System.out.print("E4 "); 
        } 
        System.out.print("F4 "); 
    } 
}

output: 
1: A4 B4 E4 F4 A 
2: A4 D4 E4 F4 B 
3: E4 E 



    public void question2() {
        try {
            System.out.print("1: ");
            perform("3");        //（1）轮进 perform call的方法 ，2轮第二次又跳出来继续往下走
            System.out.print("A ");    //（2） A出来
            System.out.println();

            System.out.print("2: ");   //（2）继续往下走
            perform("0");           // （2）轮进 perform call的方法
            System.out.print("B ");  //（3）轮  出 perform call的方法
            System.out.println();

            System.out.print("3: ");   //（3）轮
            perform(null);   //（3）轮进 perform call的方法
            System.out.print("C ");
            System.out.println();

            System.out.print("4: ");   //第四轮不会执行，第三轮已经抛出异常被捕获，程序不会再继续执行 perform("")。
            perform("");
            System.out.print("D ");
            System.out.println();
        } catch (NullPointerException e) { //  perform（）里面没有对应null的错误，向上找对应的。
            System.out.print("E ");
        } catch (Exception e) {
            System.out.print("F ");
        }
    }

    private void perform(String input) {
        try {
            int length = input.length(); //（1）input "3"    ;（2）轮 input "" ,length =1  ；（3）轮进 input: null 错 但是没有对应抓捕。
            int num1 = Integer.parseInt(input);   //（1）input "3"   //（2）轮 input ""0 ,length =1
            System.out.print("A4 ");    // （1）A4出来
            int num2 = 100 / num1;    // （1）num1:3    //（2）轮 num1 = 0
            System.out.print("B4 ");        //（1）B4出来
        } catch (NumberFormatException e) {
            System.out.print("C4 ");
        } catch (ArithmeticException e) {  //（2）轮 num1 = 0 ,抓到错误 ，打印
            System.out.print("D4 ");
        } finally {
            System.out.print("E4 ");    //（1）E4出来  ；（2）轮 E4出来   //3 轮 E4出来    ，finally必须要打印
        }
        //⁉️为什么第二轮出错的时候，finally 打印完 F4也会打印，但是第三轮不运行了？（没抓到错误？ null）,java往上👆找？
        //✅（2）的错误被内部 catch (ArithmeticException) 捕获了，异常被处理后程序继续执行 System.out.print("F4")
        // (3) 的 "F4“ 不会执行！因为执行在 try 内部的第一行就抛异常跳出了。
        System.out.print("F4 ");      //（1）F4出来 ；（2）轮 F4出来
    }

}

```


![[Pasted image 20251207013124.png]]

![[Pasted image 20251207013245.png]]


![[Pasted image 20251207013252.png]]



#### Exercise Five: Arrays and Exceptions

```java
In the `ictgradschool.industry.exceptions.arraysandexceptions` package, `ArraysAndExceptions` class contains the beginnings of a program which should generate an array of five random integers between 1-1000. The program should then allow the user to enter an index, and should print out the element in the generated array at the supplied index. Complete the program by following these steps:

1. Complete the `generateArray()` method, which should generate and return the array of random numbers.
2. Create three new classes – `InvalidIndexException`, `IndexTooLowException`, and `IndexTooHighException`. These should all be checked exceptions (i.e. extend the `Exception` class).
3. Modify the `getArrayIndexFromUser` method so that it throws these three exceptions appropriately:
   - `InvalidIndexException` should be thrown when the user doesn’t enter an integer.
     
   - `IndexTooLowException` should be thrown when the user enters a number that’s too small to be a valid index.

   - `IndexTooHighException` should be thrown when the user enters a number that’s too large to be a valid index.
     
     - ⁉️ 三个class 基本相似，不同的message ，已经接受类型，主要是在调用try catch是‘随意写’？ 总归还是要有“区分具体错误”这个功能啊，不然啥都能算“错误啦”，而这个功能就是写在main（调用异常的方法里）？
       - 主动写  throw new IndexTooLowException(-2); 这个东西是干嘛的，为什么要特别写一个“错误在方法里面” ，那这样的话，每一个我自己create的exception class 都要测试的话，那所有的class 都写上不就能万无一失的测试了么？ 比如再继续加上： throw new IndexTooHighException ，throw new InvalidIndexException ， 或者干脆写一个大的throw new Exception 能兜底全部啊
     - ✅我们不需要每个异常都“有新逻辑”， 只要有不同类型（不同 class （异常的class）名）， catch 就能区分具体是哪种错误。 只要类型匹配，系统自动进入那个块。
     - “判断什么错误发生” → 属于 方法内部（throw） “怎么应对错误” → 属于 主程序（catch）
    
    - 得自己定义规则 ?throws主动制造异常：“我主动测试或者发现”
    - try 是以防出现预测到的错误；catch 是我自己发现且调用了错误说明+应对



- exception class只是定义问题；
- 被两个地方调用
  -  getArrayIndexFromUser()（里面发现问题，throw报告问题）
  - 主程序start：match到返回上层调用，catch解决问题（循环或者打印提示）



----------------
package ictgradschool.industry.exceptions.arraysandexceptions;

import ictgradschool.Keyboard;

/**
 * A simple program that generates an array of random numbers, then displays
 * one of them (user's choice).
 */
public class ArraysAndExceptions {


    /**
     * Runs the program.
     * <p>
     * TODO Handle your InvalidIndexException, IndexTooLowException, and IndexTooHighException appropriately.
     */
    public void start() {

        //调用一个名为 generateArray() 的方法，它会“生成一个数组”，然后把返回的数组赋值给变量 myArray。
        int[] myArray = generateArray();

        // TODO Handle any exceptions generated by this line appropriately.
        // TODO If an exception is thrown, display an appropriate error message and let the user try again.

        // getArrayIndexFromUser() 提出问题， start负责循环吧
        int index = 0;
        boolean valid = false;
        while(!valid) {
            try {
                index = getArrayIndexFromUser();
                //这个boolean位置是特殊的，getArrayIndexFromUser()直接进去内部方法，
                // 即使有问题，也是直接match到start相对应的问题，然后直接退出或者print 出来 ，
                // 所以和一般的 循环boolean 不一样。 即使这个boolean条件放在了程序的开头
                valid = true;

            } catch (InvalidIndexException e) {
                System.out.println("enter a Integer");
            } catch (IndexTooLowException e) {
                System.out.println("too low");
            } catch (IndexTooHighException e) {
                System.out.println("too heigh");
            }

        }

        System.out.println("The element at index " + index + " is: " + myArray[index]);
    }





    /**
     * Gets an array index from the given user. Currently error-prone as it doesn't check whether the user
     * inputs valid numbers of the correct size.
     * <p>
     * TODO Follow these steps:
     * <ol>
     *     <li>Create three new checked Exception classes (i.e. extends Exception):
     *     <ul>
     *         <li>InvalidIndexException</li>
     *         <li>IndexTooLowException</li>
     *         <li>IndexTooHighException</li>
     *     </ul>
     *     </li>
     *     <li>Declare this method to throw these three kinds of exceptions (using the throws clause)</li>
     *     <li>Throw InvalidIndexException if the user doesn't enter an integer</li>
     *     <li>Throw IndexTooLowException if the user enters an integer that's too small to be a valid index</li>
     *     <li>Throw IndexTooHighException if the user enters an integer that's too large to be a valid index</li>
     * </ol>
     */


//⁉️ throws 写在哪？ throw提示异常的方法 ，还是处理的主程序？
    //✅ throws 写在“报告问题”的方法声明上。谁可能抛异常，谁就要 throws 说明
    //具体详细的条件下：只抛出问题 ，但是start来具体解决
    private int getArrayIndexFromUser () throws InvalidIndexException, IndexTooLowException,IndexTooHighException {

        int index =0 ;

        try{
            System.out.print("Enter an index: ");
             index = Integer.parseInt(Keyboard.readInput());

             if(index < 0){
                 throw new IndexTooLowException(index);
             }
             if(index > 4){
                 throw new IndexTooHighException(index);
             }
             return index;
             // 把系统错误换成我们自己的错误类型
            }catch(NumberFormatException e){
            throw new InvalidIndexException("Error input");
            }
    }

    /**
     * Creates and returns an array with five random numbers.
     */
    private int[] generateArray() {

        // ✅TODO Create an array of length five, and fill it with random integers between 1 - 1000.
        int [] arra = new int [5];
        System.out.println(" length is 5 ，index 0 - 4, 5=out of range");

        for(int i= 0 ; i< arra.length; i++){
            int randomNumber = (int)(Math.random() * 1000) +1 ;
            arra[i]  = randomNumber;
            System.out.println(arra[i]);
        }
        return arra;
    }

    public static void main(String[] args) {
        new ArraysAndExceptions().start();
    }

}


--------------------
package ictgradschool.industry.exceptions.arraysandexceptions;

// a number that’s too large to be a valid index.
public class IndexTooHighException extends Exception {
    public IndexTooHighException(int message) {
        super(message +"a number that’s too large to be a valid index." );
    }
}
package ictgradschool.industry.exceptions.arraysandexceptions;

// a number that’s too small to be a valid index.
public class IndexTooLowException extends Exception {
    public IndexTooLowException(int meassage) {
        super( meassage + " a number that’s too small to be a valid index ");
    }
}
package ictgradschool.industry.exceptions.arraysandexceptions;

/*我写的是一个InvalidIndexException构造器
 但是InvalidIndexException 是继承的Exception ,即使InvalidIndexException 自己接受一个int ，
 但是父类Exception 在初始化的时候只能接受String ，
 所以 在子类InvalidIndexException 里面初始化Exception 就需要转化 String into int；
    public InvalidIndexException(int a ){
        super(String.valueOf(a)); //只能是String，String.valueOf() 是一个内置的 Java 方法：
    }
    public InvalidIndexException(message a ){
        super(a);
    }
    或者，直接字符串 “” + 任何 = “”；
    public InvalidIndexException(message a ){
        super(“test” + a );
    }
*/

// thrown when the user doesn’t enter an integer.
public class InvalidIndexException extends Exception {
    public InvalidIndexException(String e){
        super( "isn’t an integer");
    }
}

```



![[Pasted image 20251207014250.png]]


![[Pasted image 20251207014303.png]]



![[Pasted image 20251207014330.png]]


![[Pasted image 20251207014346.png]]


![[Pasted image 20251207014401.png]]


![[Pasted image 20251207014422.png]]


![[Pasted image 20251207014451.png]]

![[Pasted image 20251207014532.png]]

![[Pasted image 20251207014558.png]]















--------------










**迭代（Iteration）**、**递归（Recursion）**、**枚举（Enumeration）**

#迭代（Iteration） #递归（Recursion） #枚举

**迭代（Iteration）**
![[Pasted image 20251204085453.png]]


 **递归（Recursion）**
![[Pasted image 20251204085517.png]]


**枚举（Enumeration）**
![[Pasted image 20251204085554.png]]

| **名称** | **思想核心**      | **使用工具**       | **举例**      |
| ------ | ------------- | -------------- | ----------- |
| 迭代     | 重复执行，直到结束条件成立 | 循环（for, while） | 累加、求和、遍历    |
| 递归     | 用函数自己解决更小问题   | 函数自己调用自己       | 阶乘、斐波那契、树遍历 |
| 枚举     | 穷举所有可能        | 通常结合循环或递归      | 全排列、密码爆破    |
![[Pasted image 20251204085800.png]]

|**对比维度**|**迭代（Iteration）**|**递归（Recursion）**|**枚举（Enumeration）**|
|---|---|---|---|
|思想|循环执行|自我调用|穷举所有情况|
|控制方式|使用循环控制变量|使用函数调用栈|使用循环/递归列举|
|是否有终止条件|有|有|一般有（或遍历全部）|
|优点|快、稳定|简洁优雅|能保证找到结果|
|缺点|代码长|容易栈溢出|效率低|
|常见用途|数学计算、遍历数组|分治、树结构|搜索、全排列问题|

---------



# week 5


![[Pasted image 20251209233440.png]]

![[Pasted image 20251209233434.png]]

#### DataInputStream / DataOutputStream 是什么？
![[Pasted image 20251209233530.png]]


### **缓冲流到底怎么做的**

![[Pasted image 20251209233721.png]]

>   readLine 是 BufferedReader 提供的优化方法
	它就是利用缓冲区的优势，让你 一次读取一行文本。

它的底层依然是“从缓冲区读”，不是直接读取硬盘。

## ⁉️
```
-  write() 先运行，所以 read() 能顺利读到刚写进去的数据。
如果相反呢？

- 2、 try (DataInputStream dIn = new DataInputStream(new FileInputStream(file))) {
这种写法是不是要硬背下来，不太常见？ 为什么外面是Data里面还new一个？
 概念有点奇怪 ，write = output read = input ，有点反直觉

3、 
字节流用于处理二进制数据，例如文件、图像、视频等。
字符流用于处理文本数据，例如读取和写入字符串或文件。

这两个要如何区别，我如何知道什么时候用哪一个？ 我必须要掌握的是什么方法？

```


##### ⁉️先write(file) -  output     ; 后read(file)- input   
- 为什么写是output  ,读反而是input
##### **Input / Output 的方向不是根据“执行顺序”，而是根据“数据流向”来命名的！**

![[Pasted image 20251210093452.png]]


<mark class="hltr-pink">input 和 ouput 是程序相对文件而言</mark>


##### ⁉️程序有一个`[ 1，2，3，4]`数组 。然后new了一个 char的文件，把[] output 进这个文件，然后再input 回来？ 
##### 程序的变量是临时的（程序结束就没了）
![[Pasted image 20251210093914.png]]
>变量 = 内存  
>文件 = 持久化（永久保存）


![[Pasted image 20251210093957.png]]

![[Pasted image 20251210094054.png]]









![[Pasted image 20251210084815.png]]
![[Pasted image 20251210084834.png]]


### **为什么里面 new 两次？**
![[Pasted image 20251210085053.png]]
![[Pasted image 20251210085122.png]]

![[Pasted image 20251210085144.png]]
![[Pasted image 20251210085159.png]]


![[Pasted image 20251210085212.png]]


![[Pasted image 20251210085246.png]]

![[Pasted image 20251210085353.png]]


超简单判断口诀（背下来不怕考试）：

🟩 文本 = Reader / Writer

🟦 二进制 = InputStream / OutputStream

🟥 Java 基本类型 = DataInput/OutputStream



#### **FileInputStream / FileOutputStream 很重要**

它是 **所有高级流的基础**。

![[Pasted image 20251210090226.png]]



#### **为什么不能用 File？为什么必须用 FileReader？**
![[Pasted image 20251210154023.png]]

![[Pasted image 20251210154037.png]]

![[Pasted image 20251210154047.png]]


### delimiter 作用在哪里？只作用于 Scanner

- delimiter 与 toString() 完全无关



----
#### 作业



**MyWriter = 写文件（Output） → FileWriter + PrintWriter**
**MyScanner = 读文件（Input） → File + Scanner**


```java
package ictgradschool.industry.lab08.ex02;

import ictgradschool.Keyboard;

import java.io.*;
import java.util.Scanner;

/**
 * A simple program which should allow the user to type any number of text lines. The program will then
 * write them out to a file.
 *  两个 class其实都是差不多写法 ，唯一不同的就是使用的方法？
 *
 * MyWriter = 写文件（Output） → FileWriter + PrintWriter
 *  MyScanner = 读文件（Input） → File + Scanner
 *
 *
 *
 *
 */

public class MyWriter {

    public void start() {

        System.out.print("Enter a file name: ");
        String fileName = Keyboard.readInput();

        // TODO Open a file for writing, using a PrintWriter.
        //MyWriter（写文件）
        try (
                PrintWriter ex02 = new PrintWriter(new FileWriter(fileName))) {


            while (true) {

                System.out.print("Type a line of text, or just press ENTER to quit: ");
                String text = Keyboard.readInput();

                if (text == null ||text.isEmpty()) {
                    break;
                }

                // TODO Write the user's line of text to a file.
                ex02.println(text);
            }
        } catch (IOException e) {
            System.out.println("error");
        }
        System.out.println("Done!");

    }

    public static void main(String[] args) {

        new MyWriter().start();

    }

}




/*
package ictgradschool.industry.lab08.ex02;

import ictgradschool.Keyboard;

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

        //：MyScanner（读文件）

prompt the user to enter a file name
 use a Scanner to open the file, read all the text
  print it out.

public class MyScanner {

    public void start() {

        // TODO Prompt the user for a file name, then read and print out all the text in that file.
        // TODO Use a Scanner.
        System.out.println("enter the name");
        String name = Keyboard.readInput();
        //Scanner 也可以读文件（不仅读键盘）
        try(Scanner in = new Scanner(new File(name))){

            while(in.hasNext()){
                String sth = in.nextLine();
                System.out.println(sth);
            }

        }catch(FileNotFoundException e){
            System.out.println("error " + name);
        }
    }

    public static void main(String[] args) {
        new MyScanner().start();
    }
}

 */
```


![[Pasted image 20251210203651.png]]![[Pasted image 20251210203703.png]]

![[Pasted image 20251210203724.png]]

![[Pasted image 20251210203737.png]]

![[Pasted image 20251210203751.png]]



#### movies
```java

package ictgradschool.industry.lab08.ex03;

import ictgradschool.Keyboard;

import java.io.DataOutputStream;
import java.io.FileOutputStream;
import java.io.IOException;


/**
 * Created by anhyd on 20/03/2017.
 * Complete the saveMovies method in the MovieWriter class.
 * This method should use a DataOutputStream to write the contents of the films array
 * to the given file. Note: You should not make any assumptions about
 * the number of movies in the array – your program (and the one in part 2)
 * should work for any number of movies! It might pay to write the number of movies to
 * the file, as well as the movies themselves.
 */
public class MovieWriter {

    public void start() {

        // Get a file name from the user
        System.out.print("Enter a file name: ");
        String fileName = Keyboard.readInput();

        // Create and fill Movies array
        Movie[] films = getMovieData();

        // Saves the movies
        saveMovies(fileName, films);
    }

    /**
     * Saves the movies to the given file.
     */
    protected void saveMovies(String fileName, Movie[] films) {

        // TODO Implement this method
        //filems [] ，需要进file ，循环？ 还有length
        try(DataOutputStream m = new DataOutputStream(new FileOutputStream(fileName))){
            int lengthMo = films.length;
            //writeInt() 写入的不是“数组”，而是一个普通的 int 数字。
            //??⁉️为什么必须写在文件开头？可不可以写在结尾？中间？
                m.writeInt(lengthMo);

            for(int i = 0; i< films.length ;i++){
                m.writeUTF(films[i].getName());
                m.writeInt(films[i].getYear());
                m.writeInt(films[i].getLengthInMinutes()); ;
                m.writeUTF(films[i].getDirector());

            }

        }catch(IOException e ){

            System.out.println("error" + e.getMessage());
        }

        System.out.println("Movies saved successfully to " + fileName + "!");
    }

    /**
     * Returns an array with a bunch of hard-coded movie data
     */
    private Movie[] getMovieData() {
        Movie[] films = new Movie[19];
        films[17] = new Movie("The Intouchables", 2011, 112, "Olivier Nakache and Eric Toledano");
        films[6] = new Movie("From Russia With Love", 1963, 110, "Terence Young");
        films[14] = new Movie("The Long Voyage Home", 1940, 105, "John Ford");
        films[9] = new Movie("Easy Rider", 1969, 94, "Dennis Hopper");
        films[3] = new Movie("Dark Shadows", 2012, 113, "Tim Burton");
        films[10] = new Movie("Walk the Line", 2005, 136, "James Mangold");
        films[5] = new Movie("The Help", 2011, 137, "Tate Taylor");
        films[0] = new Movie("Meet the Parents", 2000, 107, "Jay Roach");
        films[7] = new Movie("The King's Speech", 2011, 118, "Tom Hooper");
        films[8] = new Movie("Charlie and the Chocolate Factory", 2005, 115, "Tim Burton");
        films[2] = new Movie("Alice In Wonderland", 2009, 109, "Tim Burton");
        films[4] = new Movie("The Iron Lady", 2011, 105, "Phylliday Lloyd");
        films[11] = new Movie("Kaikohe Demolition", 2004, 52, "Florian Habicht");
        films[12] = new Movie("Brokeback Mountain", 2005, 134, "Ang Lee");
        films[13] = new Movie("Gladiator", 2000, 154, "Ridley Scott");
        films[1] = new Movie("The Parent Trap", 1961, 129, "David Swift");
        films[15] = new Movie("Happy-Go-Lucky", 2008, 118, "Mike Leigh");
        films[16] = new Movie("The Big Wedding", 2013, 89, "Justin Zackham");
        films[18] = new Movie("Searching for Sugar Man", 2012, 86, "Malik Bendjelloul");
        return films;
    }

    public static void main(String[] args) {
        new MovieWriter().start();
    }
}

```


##### ⁉️writeInt(films.length) 本质上 **就是写入一个普通的 int**。
![[Pasted image 20251210210734.png]]
![[Pasted image 20251210210835.png]]




![[Pasted image 20251210210848.png]]

![[Pasted image 20251210215212.png]]



----
### Lab 9 - Collections 


