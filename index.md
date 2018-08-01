---
layout: default
---

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

The downside to using arrays is that they don't provide much functionality. The only thing you can do with an array is store a known-number of objects. Additionally, the array can only tell you how long it is, and what object is at a certain index. The syntax is as follows:

```java
int[] numbers = {1, 2, 3, 4, 5};

// If we print the length of the array...
System.out.println(numbers.length); // produces 5

// If we want to print what is at a given index...
System.out.println(numbers[0]); // produces 1
System.out.println(numbers[1]); // produces 2
System.out.println(numbers[2]); // produces 3
System.out.println(numbers[3]); // produces 4
System.out.println(numbers[4]); // produces 5
```

> TIP: To **print** something to the console, use the `System.out.println()` function.


#### Data Types

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Data Types

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Data Types

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
