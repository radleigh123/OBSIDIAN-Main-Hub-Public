---
cssclass: 
- t-c
- tbl-nalt
- t-w
title: JavaVariables
creation-date: 2023-02-03
aliases:
tags:
- Java/Lecture
- Java/String
---
**[[Java|HOME [Java]]]**

---
# Variables
**Primitive data types**
There are eight primitive data types in Java:
- four are for integer values;
- two are for values with a decimal point;
- one is for storing single characters, and;
- one is for Boolean data that allows only either true or false as a value.

| PRIMITIVE TYPE | SIZE              | MIN VALUE       | MAX VALUE                        | WRAPPER CLASS |
| -------------- | ----------------- | --------------- | -------------------------------- | ------------- |
| `byte`         | 8 bits / 1 byte   | -128            | 127                              | **Byte**      |
| `short`        | 16 bits / 2 bytes | -32,768         | 32,767                           | **Short**     |
| `int`          | 32 bits / 4 bytes | -2,147,483,648  | 2,147,483,647                    | **Integer**   |
| `long`         | 64 bits / 8 bytes | -9,223,372,036, | 9,223,372,036,                   | **Long**      |
|                |                   | 854,775,808     | 854,775,807                      |               |
| `float`        | 32 bits / 4 bytes | 6-7 digits      | 6-7 digits                       | **Float**     |
| `double`       | 64 bits / 8 bytes | 15 digits       | 15 digits                        | **Double**    |
| `char`         | 16 bits / 2 bytes           | Unicode 0       | Unicode 2 in a power of 16 value | **Character** |
| `boolean`      | -                 | false (not min) | true (not max)                   | **Boolean**   |

^3c12e4

**e.g.**
```java
int intNum = 123456789;
long longNum = 123456L; // `L` at the end

float floatNum = 3.14f; // `f` at the end
double doubleNum = 3.15;

char var2 = 'A';
boolean var1 = true; // or false
```

<br>

**Reference data types**

| data type | size   | value                                   |
| --------- | ------ | --------------------------------------- |
| `String`  | varies | a sequence of characters, **"Hello World"** | 

**e.g.**
```java
String var3 = "Hello World"; // anything reference data type begins Capital
```

<br>

>[!FAQ|c-blue alt-co collapse no-i]+ FAQ
>>[!column|clean no-t collapse]
>>>[!INFO|clean no-i collapse] Primitive
>>> ◾ stores data
>>> ◾ can only hold 1 value
>>> ◾ less memory
>>> ◾ fast
>>
>>>[!INFO|clean no-i collapse] Reference
>>> ◾ stores an address, unlimited (user-defined)
>>> ◾ could hold more value
>>> ◾ more memory
>>> ◾ slower
>

Examples:
- [[JavaVariablessample0|Swapping Variables Program]]

<br>

# 
---
**Sources:**
-  **Data types** - https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html
- **String** - https://docs.oracle.com/javase/7/docs/api/java/lang/String.html