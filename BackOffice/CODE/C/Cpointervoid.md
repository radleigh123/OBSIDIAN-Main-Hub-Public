---
aliases:
tags:
- C/Lecture
- C/Pointers
- C/Typecasting
---
**[[C|HOME [C]]]**

---
## Pointer Void
A pointer to void means a generic pointer that can point to any data type.
**Syntax:** `void *pointer_name;`
```C
int i = 9; // integer variable initialization.
int *p; // integer pointer declaration.
float *fp; // floating pointer declaration.
void *ptr; // void pointer declaration.

p = fp; // incorrect, p is an `integer pointer`
fp = &i; // incorrect, fp is a `floating pointer`

ptr = p; // correct
ptr = fp; // correct
ptr = &i; // correct
```

**Dereferencing a void pointer**
```C
#include <stdio.h>

int main()
{
   int a=90;
   void *ptr;
   ptr=&a;

   printf("Value which is pointed by ptr pointer : %d",*(int*)ptr);
   // typecasting is needed to turn void pointer into integer pointer
   return 0;
}
```

>[!INFO] Why we use `void` pointer
> We use void pointers because of its reusability. Void pointers can store the object of any type, and we can retrieve the object of any type by using the indirection operator with proper typecasting.
> **e.g.**
> ```C
> #include<stdio.h>
> int main()
> {
> 	int a=56; // initialization of a integer variable 'a'
> 	float b=4.5; // initialization of a float variable 'b'
> 	char c='k'; // initialization of a char variable 'c'
> 	void *ptr; // declaration of void pointer
>    
> 	// assigning the address of variable 'a'
> 	ptr=&a;
> 	printf("value of 'a' is : %d",*((int*)ptr));
>
> 	// assigning the address of variable 'b'.
> 	ptr=&b;
> 	printf("\nvalue of 'b' is : %f",*((float*)ptr));
>    
> 	// assigning the address of variable 'c'.
> 	ptr=&c;
> 	printf("\nvalue of 'c' is : %c",*((char*)ptr));
>
> 	return 0;
> }
> ```

<br>

# 
---
**Sources:**
- [Void Pointer in C - javatpoint](https://www.javatpoint.com/void-pointer-in-c)