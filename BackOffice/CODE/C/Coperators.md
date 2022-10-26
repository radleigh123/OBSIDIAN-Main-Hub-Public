---
title: Operators
creation-date: 2022-10-25
aliases: [increment, decrement]
tags:
- C/Operators
---
**[[C|HOME [C]]]**

# Operators
### Increment & Decrement Operators
- You cannot use **[rvalue](Cleftrightvalue.md)** before or after increment/decrement operator
```C
(a + b)++; // error!
++(a + b); // error!

(a+b)++;
(a+b) = (a+b) + 1;
```
![[Pasted image 20221007150335.png|650]]

<br>

# 
---
**Source:**
- [Increment and Decrement Operators in C (Part 1) - YouTube](https://www.youtube.com/watch?v=Lpo1QYsuAmM&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=25)