---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Initializing an Array
A variable that has a primitive type, such as `int`, holds a value. A variable with a reference type, such as an array, holds a memory address where a value is stored. In other words, array names contain references, as do all Java object names. 

No memory address is assigned when you declare an array using only a data type, brackets, and a name. Instead, the array variable name has the value null, which means the identifier is not associated with a memory address. You can explicitly assign null to an array reference, but it is not required. For example, each of the following statements assigns null to `someNums`:
```java
int[] someNums;  
int[] someNums = null;  
```
When you use the keyword new to define an array, the array reference acquires a memory address value. For example, when you define `someNums` in the following statement, a memory address is assigned:
```java
int[] someNums = new int[10];
```
When you declare `int[] someNums = new int[10];`, `someNums` holds an address, but each element of `someNums` has a value of 0 by default because `someNums` is an integer array. Each element in a double or float array is assigned 0.0. By default, char array elements are assigned `\u0000`, which is the Unicode value for a null character, and boolean array elements automatically are assigned the value false. In arrays of objects, including Strings, each element is assigned null by default.

You already know how to assign a different value to a single element of an array, as in:
```java
someNums[0] = 46;
```
You can also assign non-default values to array elements upon creation. To initialize an array, you use an initialization list of values separated by commas and enclosed within curly braces. Providing values for all the elements in an array also is called populating the array. 

For example, if you want to create an array named `multsOfTen` and store the first six multiples of 10 within the array, you can declare the array as follows:
```java
int[] multsOfTen = {10, 20, 30, 40, 50, 60};
```
Notice the semicolon at the end of the statement. You don’t use a semicolon following a method’s closing curly brace, but you do use one following the closing brace of an array initialization list.

When you populate an array upon creation by providing an initialization list, you do not give the array a size—the size is assigned based on the number of values you place in the initializing list. For example, the `multsOfTen` array just defined has a size of 6. Also, when you initialize an array, you do not need to use the keyword new; instead, new memory is assigned based on the length of the list of provided values.

In Java, you cannot directly initialize part of an array. For example, you cannot create an array of 10 elements and initialize only five; you either must initialize every element or none of them.