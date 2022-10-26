---
title: Variables
creation-date: 2022-10-25
aliases: [local, global, static, automatic, external]
tags:
- C
- C/lecture 
---
**[[C|HOME [C]]]**

# Variables
> is a name of the memory location.
>- It is used to store data.
>- Its value can be changed
>- It can be reused many times.
>
>> **Syntax:** `type variableList;`
>
>>[!EXAMPLE]- 
>> ```C
>> int a;
>> float b;
>> char c = 'A'; //declaring 1 variable of char type
>> ```

>[!TIP]- Rules of Defining variables
>>[!CHECK]
>>- A variable can have alphabets, digits, and underscore.
>> ```C
>> int a;
>> int _ab;
>> int a30;
>> ```
>
>>[!FAIL]
>>- A variable name can start with the alphabet, and underscore only. It can't start with a digit.
>> ```C
>> int 2;
>> ```
>>- No whitespace is allowed within the variable name.
>> ```C
>> int a b;
>> ```
>>- A variable name must not be any reserved word or keyword, e.g. int, float, etc.
>> ```C
>> int long;
>> ```

### Types of Variables in C
- Local variable
- Global variable
- Static variable
- Automatic variable
- External variable