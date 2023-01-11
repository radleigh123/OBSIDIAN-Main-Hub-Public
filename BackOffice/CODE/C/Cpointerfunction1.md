---
aliases:
tags:
- C/Lecture
- C/Pointers/Functions
---
**[[C|HOME [C]]]**

---
## Function pointer
**Syntax:** `return_type (*ptr_name) (type1, type2, ...);`
```C
float (*fp)(int, int); // Declaration of a function pointer
float func(int, int); // Declaration of a function
fp = func; // Assigning address of func to the fp pointer

result = (*fp)(a, b); // Calling a function using function pointer or...
/*
result = fp(a, b);
*/
```
**e.g.**
```C
#include <stdio.h>
int add(int, int);

int main()
{
	int a, b;
	int (*ip)(int, int);
	int result;

	printf("Enter the values of a and b : ");
	scanf("%d %d", &a, &b);

	ip = add;
	result = (*ip)(a, b);

	printf("Value after addition is : %d", result);
	return 0;
}

int add(int a, int b)
{
	int c = a + b;
	return c;
}
```

<br>

# 
---
**Sources:**
- [C function Pointer - javatpoint](https://www.javatpoint.com/c-function-pointer)