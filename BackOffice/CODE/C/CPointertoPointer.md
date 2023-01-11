---
aliases:
tags:
- C/Lecture
- C/Pointers
---
**[[C|HOME [C]]]**

---
## Pointer to pointer
Such pointer is known as a double pointer (pointer to pointer). The first pointer is used to store the address of a variable whereas the second pointer is used to store the address of the first pointer. ![[Pasted image 20230104164147.png|center]]
**Syntax:** `int **ptr`
```C
#include<stdio.h>

int main ()
{
    int a = 10;
    int *p;
    int **pp; 
    p = &a; // pointer p is pointing to the address of a
    pp = &p; // pointer pp is a double pointer pointing to the address of pointer p

    printf("address of a: %x\n",p); // Address of a will be printed 
    printf("address of p: %x\n",pp); // Address of p will be printed
    printf("value stored at p: %d\n",*p); // value stoted at the address contained by p i.e. 10 will be printed
    printf("value stored at pp: %d\n",**pp); // value stored at the address contained by the pointer stoyred at pp

    return 0;
}
```

<br>

# 
---
**Sources:**
- [C Pointer to Pointer - javatpoint](https://www.javatpoint.com/c-pointer-to-pointer)