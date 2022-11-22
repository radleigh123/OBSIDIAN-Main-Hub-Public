---
aliases:
tags:
- C/Variables
---
**[[Cvariables#Types of Variables in C|BACK]]**

---
## External Variable
We can share a variable in multiple C source files by using an external variable. To declare an external variable, you need to use **extern keyword**.

*myfile.h*
```C
extern int num1 = 10; //external variable (also global)
```

<br>

*program1.c*
```C
#include<stdio.h>
#include"myfile.h"
void printValue(){
	printf("Global variable: %d", global_variable)
}
```