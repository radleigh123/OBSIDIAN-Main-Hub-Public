---
cssclass: no-m
title: Functions
creation-date: 2022-10-26
aliases:
tags:
- C/Functions/Return_Function
- C/Lecture
---
**[[C|HOME [C]]]**

---
# Functions
>- is a block of code which only runs when it is called.
>- You can pass data, known as parameters, into a function.

## Syntax
```C
void myFunction() {
	printf("Hello World");
}

int main(){
	myFunction(); // call the function
	
	return 0;
}
```
>[!INFO]+ Function aspects
>- **Function declaration** A function must be declared globally in a c program to tell the compiler about the function name, function parameters, and return type. e.g. `return_type function_name (argument list);`
>- **Function call** We must pass the same number of functions as it is declared in the function declaration. e.g. `function_name (argument_list)`
>- **Function definition** Here depending on the code, we must notice that only one value can be returned from the function.
>```C
>return_type function_name (argument list) {
>	function body;
>}
>```

## Sample
```C
#include<stdio.h>

int addNumbers(int, int);

int main(){
    int n3, n4, result;
    printf("Enter two integers: ");
    scanf("%d%d", &n3, &n4);

    // return value is stored in result
    result = addNumbers(n3, n4);
    printf("Sum = %d", result);

    return 0;
}

int addNumbers(int n1, int n2){
    int sum;
    sum = n1 + n2;
    
    return sum;
}
```

# 

<br>

---
**Sources:**
- [C Functions (w3schools.com)](https://www.w3schools.com/c/c_functions.php)
- [Functions in C - javatpoint](https://www.javatpoint.com/functions-in-c)