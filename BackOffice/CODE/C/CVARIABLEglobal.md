---
aliases:
tags:
- C/Variables
---
**[[Cvariables#Types of Variables in C|BACK]]**

---
## Global Variable
A variable that is declared outside the function or block is called a global variable. Any function can change the value of the global variable. It is available to all the functions.
```C
int value = 20; //global variable

void function1(){
	int num1 = 10; //local variable
}
```