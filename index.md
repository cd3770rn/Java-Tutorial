---
layout: default
---

### A Short History of Programming Languages
Computers obviously do not understand human languages, so programs are written in a language that a computer can use. There are many programming languages, all of which a computer can recognize. In order for the computer to understand these commands, they must be first converted into instructions the computer can use.


#### Machine Code
The lowest level of programming languages is machine code, better known as binary. In order to provide a command for the computer to use, it must be written as a series of zeroes and ones. For example, to add two numbers, you might have to write an instruction in binary code like this: 
```
1101101010011010
```

#### Assembly Language
As you can probably guess, programming in binary is tedious and difficult. Programs written in binary are very difficult to decipher, and equally as hard to modify. Assembly language was created to solve this problem. Assembly uses a mnemonic to represent instructions for the computer. Instead of writing a bunch of zeroes and ones, you can now write:
```
add 2, 3, result
```
    
Assembly was made to allow humans to more easily write code. Much like higher-level languages, however, the computer cannot execute code written in assembly. An **assembler** is used to translate assembly-language programs into machine code that the computer *can* execute. So writing `add 2, 3, result` will be converted to `1101101010011010` and the computer will perform the command. 

While much easier than binary, writing code in assembly language is still time consuming and challenging. Writing in assembly requires that you understand how the CPU works. It is therefore considered a low-level language.

#### High-Level Languages

High-level languages came about in the 1950s, and allow the programmer to write code that is platform independent. That is, you can write code in a high-level language and it can be executed on different types of machines. They also offer other benefits such as GUI-based development environments and are much more powerful when compared to low-level languages.


* * *

**Data structures**, or _data types_, are used to store information in a program. Java, like all high-level languages, provides a number of built-in data types that are available for you to use right away. **Object-oriented programming**, or **OOP**, allows for simple data types to be used to create a more useful complex data structure, such as a user profile.

* * *

### Data Types
* **boolean** – a true or false value
* **byte** – 8-bit signed integer with possible values between -128 and 127 (inclusive)
* **short** – 16-bit signed integer with possible values between -32,768 and 32,767 (inclusive)
* **int** – 32-bit signed integer with possible values between -2<sup>31</sup> and 2<sup>31</sup>-1
* **long** – 64-bit signed integer with possible values between -2<sup>63</sup> and 2<sup>63</sup>-1
* **float** – 32-bit signed floating-point value with 6 to 9 digits of precision _(ex. '1.53')_
* **double** – 64-bit signed floating-point value with 15 to 17 digits of precision
* **char** – a single 16-bit Unicode character stored between two single-quotes _(ex. 'a')_
* String – any sequence of Unicode characters stored between two double-quotes _(ex. "a1b2c")_

> Note that Strings are not _technically_ data types in Java. Instead, they are considered to be an **array** of characters.

* * *

### Variables
While data types _store_ information, variables serve as a way to _reference_ information. Java is a strongly-typed language, meaning that in order to create a variable, you must first specify its data type.

To **declare**, or _create_ a variable, the **syntax**, or _way it is written_, is as follows:
```java
datatype variablename = value;
```
> Every statement in Java must be follwed by a semicolon to denote the end of the statement.
> Note that your variables cannot share the name of already existing variables, funtions, or classes.

So, to create a **boolean** called **myBoolean** which is **true**, the syntax is as follows:
```java
boolean myBoolean = true;
```
The process is similar for creating a variable of any other type:
```java
byte myByte = 123;
short myShort = 1234;
int myInt = 1234567;
long myLong = 1234567890;
```

Modern computers have more available memory than they did in the past, so Java assumes all floating point-values are of type **double** _(64-bit floating-point number)_ unless otherwise specified. To create a **float** _(32-bit floating-point number)_, you must add an _f_ to the end of a floating-point value.
```java
float myFloat = 1.23456f;
double myDouble = 1.23456;
```

Declaring character variables is written the same way as for other data types:
```java
char myChar = 'a';
```
> Note that to declare a String, you must use a capital S.
> This is because Strings are considered Objects, and are not considered a primitive _(built-in)_ data type.
> This is also why you will not see the word _'String'_ formatted like other data types.

```java
String myString = "abc123";
```

* * *

### Data Structures
In addition to these data types, there are built-in data structures as well. They offer basic ways to store data. Unlike humans, computers begin counting from 0, so the first object in a data structure has an **index**, or _number pertaining to its order in the data structure_, of 0. The simplest data structure is an array, which is declared as follows:


```java
// If you know exactly what you want in the array when you define it...
datatype[] name = {value, value, value};

// Otherwise you can define how large an array is like this...
datatype[] name = new datatype[size];
```

The downside to using arrays is that they don't provide much functionality. The only thing you can do with an array is store a known-number of objects. Additionally, the array can only tell you how long it is, and what object is at a certain index. 

Given the following array:
```java
int[] numbers = {1, 2, 3, 4, 5};
```

We can check the length like this:
```java
System.out.println("===== LENGTH OF THE ARRAY =====");
System.out.println(numbers.length); 
```
Which, as expected, produces the length of the array:
```java
===== LENGTH OF THE ARRAY =====
5
```

And we can find what object is at a given index like this:
```java
System.out.println("===== OUTPUT =====")
System.out.println(numbers[0]); // print index 0
System.out.println(numbers[1]); // print index 1
System.out.println(numbers[2]); // ...
System.out.println(numbers[3]); // ...
System.out.println(numbers[4]); // ...
```

And we will get the following output:
```java
===== OUTPUT =====
1
2
3
4
5
```
> TIP: To **print** something to the console, use the `System.out.println()` function.

* * *

### Operators

There are many different operators in Java, which are shared by most languages in one form or another.

#### Arithmetic Operators

| Operator        | Description          | Example |
|:-------------|:------------------|:------|
| + _(Addition)_           | Adds values on either side of the operator. | 10 + 20 = 30  |
| - _(Subtraction)_ | Subtracts right-hand operand from left-hand operand.   | 10 - 20 = -10  |
| ∗ _(Multiplication)_           | Multiplies values on either side of the operator.      | 10 ✱ 20 = 200   |
| / _(Division)_           | Divides left-hand operand by right-hand operand. | 20 / 10 = 2  | 
| % _(Modulus)_           | Divides left-hand operand by right-hand operand and returns remainder. | 20 % 10 = 0  | 
| ++ _(Increment)_           | Increases the value of the operand by 1. | 20++ becomes 21  | 
| -- _(Decrement)_           | Decreases the value of the operand by 1. | 20-- becomes 19  | 

#### Relational Operators

| Operator        | Description          | Example |
|:-------------|:------------------|:------|
| == _(Equal to)_           | Checks if the value of both operands are equal. Returns true or false. | 10 == 20 returns false  |
| != _(Not equal to)_           | Checks if the value of both operands are not equal. Returns true or false. | 10 != 20 returns true  |
| > _(Greater than)_           | Checks if the value of the left operand is greater than the value of the right operand. Returns true or false. | 10 > 20 returns false  |
| < _(Less than)_           | Checks if the value of the left operand is less than the value of the right operand. | 10 < 20 returns true  |
| >= _(Greater than or equal to)_           | Checks if the value of the left operand is greater than or equal to the right operand. Returns true or false. | 10 >= 20 returns false  |
| <= _(Less than or equal to)_           | Checks if the value of the left operand is less than or equal to the right operand. Returns true or false. | 10 <= 20 returns true  |

#### Logical Operators

| Operator        | Description          | Example |
|:-------------|:------------------|:------|
| && _(Logical AND)_           | Checks if both operands are true. Returns true or false. | true && false returns false  |
| ∥ _(Logical OR)_           | Checks if any operand is true. Returns true or false. | true ∥ false returns true  |
| ! _(Logical NOT)_           | Used to reverse the logical state of its operand. If a condition is true, then a logical NOT will make it false. | !(true && false) returns true  |

#### Assignment Operators

| Operator        | Description          | Example |
|:-------------|:------------------|:------|
| =           | Assignment operator. Assigns values from right side operands to left side operand. | A = 10 + 20  |
| +=            | Addition and assignment operator. Adds right operand to the left operand and then assigns the result to the left operand. | A += 10 _(equivalent to A = A + 10)_ |
| -=            | Addition and subtraction operator. Subtracts right operand from the left operand and assigns the result to the left operand. | A -= 10 _(equivalent to A = A - 10)_ |
| ∗=            | Multiplication and assignment operator. Multiplies right operand with the left operand and assigns the result to the left operand. | A ∗= 10 _(equivalent to A = A ∗ 10)_  |
| /=           | Division and assignment operator. Divides left operand with the right operand and assigns the result to the left operand. | A /= 2 _(equivalent to A = A / 10)_  |
| %=           | Modulus and assignment operator. It takes modulus using two operands and assigns the result to the left operand. | A %= 3 _(equivalent to A = A % 3)_ |

#### Miscellaneous Operators

| Operator        | Description          | Example |
|:-------------|:------------------|:------|
| ? :           | This operator consists of three operands and is used to evaluate boolean expressions. The goal of the operator is to decide which value should be assigned to the variable. | int x = (expression) ? _(value if true)_ : _(value if false)_  |
| instanceof           | This operator is used only for object reference variables. The operator checks whether the object is of a particular type (class type or interface type). | 7.5 instanceof int returns false  |

* * *

### Syntax

Having an idea and knowing how to execute it are completely separate challenges. Syntax is the way in which things are written, and knowing and understanding it is pertinent to your ability to code. As mentioned above, Java is a strongly typed language. This means you need to do things how Java expects you to, or you will have errors in your code. 

In most programming languages, variable and function names are written in **Camel Case**. When using camel case, the first letter of a variable or function is lowercase, with every subsequent word being capitalized. Here's an example:

```java
// Camel Case
int numberOfDogs = 4;
double slicesOfPizza = 6.5;

//Not in Camel Case
int numberofcats = 2;
String yarn = "Hello World!";
```


Each statement in Java requires a semicolon at the end of each line, regardless of if you are declaring a variable or **calling**, or _(accessing)_, a function.

```java
int cats = 3;
int dogs = getNumberOfDogs();
```
