---
title: C++basicoperations
creation-date: 2023-01-07
aliases:
tags:
- CPP/Lecture
- CPP/Operators
- CPP/Conversion/Typecasting
- CPP/Conversion/Narrowing_conversion
---
**[[C++|HOME [C++]]]**

---
# Basic Operations
>[!column|clean collapse no-t]
>>[!INFO|clean no-t txt-c]
>> **Addition**
>> `return_type var0 = var1 + var2;`
>> **Subtraction**
>> `return_type var0 = var1 - var2;`
>> **Multiplication**
>> `return_type var0 = var1 * var2;`
>
>>[!INFO|clean no-t txt-c]
>> **Division**
>> `return_type var0 = var1 / var2;`
>> **Modulo**
>> `return_type var0 = var1 % var2;`

>[!INFO|alt-co]+ typecasting conversion
> ```cpp
> #include <iostream>
> 
> int main()
> {
>     int num1{22 / 3}, num2{3};
>     
>     std::cout << (double)num1 / num2 << std::endl;
>         return 0;
> }
> ```