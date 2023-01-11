---
aliases:
tags:
- C/Lecture
- C/Pointers
- C/stddef
---
**[[C|HOME [C]]]**

---
## Pointer Null
is a pointer that does not point to any memory location. It stores the base address of the segment. The null pointer basically stores the Null value while void is the type of the pointer.
**e.g.**
>[!column|clean no-t collapse]
>>[!INFO|clean no-t]
>> `int *ptr = (int *)0;`
>> `float *ptr = (float *)0;`
>> `char *ptr = (char *)0;`
>
>>[!INFO|clean no-t]
>> `double *ptr = (double *)0;`
>> `char *ptr = '\0';`
>> `int *ptr = NULL;`

```C
#include <stdio.h>
int main()
{
    int *ptr;
    ptr = (int*)malloc(4*sizeof(int));

    if(ptr == NULL) printf("Memory is not allocated");
    else printf("Memory is allocated");

    return 0;
}
```

>[!NOTE|alt-co] It is always a good practice that we assign a Null value to the pointer when we do not know the exact address of memory.

<br>

# 
---
**Sources:**
- [Null Pointer in C - javatpoint](https://www.javatpoint.com/null-pointer-in-c)