---
title: Cprintfscanf
creation-date: 2022-10-25
aliases:
tags:
- C/stdio/scanf
- C/Lecture
---
**[[C|HOME [C]]]**

# `printf()` and `scanf()`
Both functions are inbuilt library functions, defined in [[Cstdioh|stdio.h]] (header file)

### `printf()` function
> is used to for output. It prints the given statement to the console.
> The **format string** can be %d (integer), %c (character), %s (string), %f (float) etc.
>> **Syntax:** `printf("formatString", argumentList);`

---
### `scanf()` function
> is used for input. It reads the input data from the console.
>> **Syntax:** `scanf("formatString", argumentList);`

- doesn't store the white space characters in the string variable
	- ![[Pasted image 20220924224946.png]]