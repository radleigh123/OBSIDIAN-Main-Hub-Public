---
cssclass: t-c, tbl-nalt
title: Javavariables
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

| data type | size    | value                              |
| --------- | ------- | ---------------------------------- |
| `boolean` | 1 bit   | true/false                         |
| `byte`    | 1 byte  | -128 - 127                         |
| `short`   | 2 bytes | -32,768 - 32,767                   |
| `int`     | 4 bytes | -2 billion - 2 billion             |
| `long`    | 8 bytes | -9 quintillion - 9 quintillion     |
|           |         |                                    |
| `float`   | 4 bytes | 6-7 digits, e.g. **3.123456f**     |
| `double`  | 8 bytes | 15 digits, e.g. **3.123456789...** |
|           |         |                                    |
| `char`    | 2 bytes | single characters, **f**           | 

**Reference data type**

| data type | size   | value                                   |
| --------- | ------ | --------------------------------------- |
| `String`  | varies | a sequence of characters, **"Hello World"** | 

>[!FAQ|bg-c-purple]+ FAQ
>>[!column|clean no-t collapse]
>>>[!INFO|clean no-i ttl-c collapse] Primitive
>>> ◾ 8 types (boolean, byte, etc.)
>>> ◾ stores data
>>> ◾ can only hold 1 value
>>> ◾ less memory
>>> ◾ fast
>>
>>>[!INFO|clean no-i ttl-c collapse] Reference
>>> ◾ unlimited (user-defined)
>>> ◾ stores an address
>>> ◾ could hold more value
>>> ◾ more memory
>>> ◾ slower

**e.g.**
```cpp
int num1 = 123456789;
float num2 = 3.14f; // `f` at the end
double num3 = 3.15;

boolean var1 = true; // or false
char var2 = 'A';
String var3 = "Hello World"; // anything reference data type begins Capital

// Printing variables in single line
System.out.println("num1: " + var3 + " " + num2);
```
---
- [[JavaVariablessample0|program to swap variables]]

<br>

# 
---
**Sources:**
-  **Data types** - https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html
- **String** - https://docs.oracle.com/javase/7/docs/api/java/lang/String.html