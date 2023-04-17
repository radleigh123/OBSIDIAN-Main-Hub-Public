---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Declaring Arrays
An array is a named list of data items that all have the same data type. Each data item is an element of the array. You declare an array variable in the same way you declare any simple variable, but you insert a pair of square brackets after the type. For example, to declare an array of double values to hold sales figures for salespeople, you can write the following:
```java
double[] salesFigures;
```
Similarly, to create an array of integers to hold student ID numbers, you can write the following:
```java
int[] idNums;
```
You can provide any legal identifier you want for an array, but Java programmers conventionally name arrays by following the same rules they use for variables—array names start with a lowercase letter and use uppercase letters to begin subsequent words. Additionally, many programmers observe one of the following conventions to make it more obvious that the name represents a group of items:
- Arrays are often named using a plural noun such as *salesFigures*.
- Arrays are often named by adding a final word that implies a group, such as *salesList*, *salesTable*, or *salesArray*.

After you create an array variable, you still need to reserve memory space. You use the same procedure to create an array that you use to create an object. Recall that when you create a class named Employee, you can declare an Employee object with a declaration such as:
```java
Employee oneWorker;
```
However, that declaration does not actually create the `oneWorker` object. You create the `oneWorker` object when you use the keyword new and a call to the constructor, as in:
```java
oneWorker = new Employee();
```
Similarly, declaring an array and reserving memory space for it are two distinct processes. To reserve memory locations for 20 `salesFigures` values, you can declare the array variable and create the array with two separate statements as follows:
```java
double[] salesFigures;
salesFigures = new double[20];
```
Alternatively, just as with objects, you can declare and create an array in one statement with the following:
```java
double[] salesFigures = new double[20];
```
The statement `double[] salesFigures = new double[20];` reserves 20 memory locations for 20 double values. You can distinguish each `salesFigures` item from the others with a subscript. A **subscript** is an integer contained within square brackets that specifies one of an array’s elements. In Java, any array’s elements are numbered beginning with 0, so you can legally use any subscript from 0 through 19 when working with an array that has 20 elements. In other words, the first `salesFigures` array element is `salesFigures[0]` and the last `salesFigures` element is `salesFigures[19]`. Figure 8-1 shows how the first few and last few elements of an array of 20 `salesFigures` values appear in computer memory.

![[COMPROG12LECSEMIch11.png|center]]

It is a common mistake to forget that the first element in an array is element 0, especially if you know another programming language in which the first array element is element 1. Making this mistake means you will be “off by one” in your use of any array. It is also common to forget that the last element’s subscript is one less than the array’s size and not the array’s size. For example, the highest allowed subscript for a 100-element array is 99. To remember that array elements begin with element 0, it might help if you think of the first array element as being “zero elements away from” the beginning of the array, the second element as being “one element away from” the beginning of the array, and so on. If you use a subscript that is too small (that is, negative) or too large for an array, the subscript is out of bounds and an error message is generated.

When you work with any individual array element, you treat it no differently than you would treat a single variable of the same type. For example, to assign a value to the first `salesFigures` element in an array, you use a simple assignment statement, such as the following:
```java
salesFigures[0] = 2100.00;
```
To display the last `salesFigures` element in an array of 20, you can write:
```java
System.out.println(salesFigures[19]);
```
When programmers talk about these statements, they typically say things like, “*`salesFigures` sub zero is assigned 2100.00,*” and “*`salesFigures` sub 19 is output.*” In other words, they use sub as shorthand for “with the subscript.”

When you declare or access an array, you can use any expression to represent the size, as long as the expression is an integer. Some other programming languages, such as C++, allow only named or unnamed constants to be used for the size when an array is declared. Java allows variables, arithmetic expressions, and method return values to be used as array sizes, which makes array declaration more flexible.

For example, to declare a double array named moneyValues, you might use any of the following:

$\quad$◾ A literal integer constant; for example:
```java
double[] moneyValues = new double[10];
```
$\quad$◾ A named integer constant; for example:
```java
double[] moneyValues = new double[NUMBER_ELS];
```
In this example, the constant NUMBER_ELS must have been previously declared and assigned a value.

$\quad$◾ An integer variable; for example:
```java
double[] moneyValues = new double[numberOfEls];
```
In this example, the variable numberOfEls must have been previously declared and assigned a value.

$\quad$◾ A calculation; for example:
```java
double[] moneyValues = new double[x + y * z];
```
In this example, the variables x, y, and z must have been previously declared and assigned values, and the result of the expression x + y * z must be an integer.

$\quad$◾ A method’s return value; for example:
```java
double[] moneyValues = new double[getElements()];
```
In this example, the method getElements() must return an integer.