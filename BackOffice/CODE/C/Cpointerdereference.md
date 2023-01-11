---
aliases:
tags:
- C/Lecture
- C/Pointers
---
**[[C|HOME [C]]]**

---
## Pointer Dereference
also known as an indirection operator, which is represented by (\*). When we dereference a pointer, then the value of the variable pointed by this pointer will be returned.
```C
#include <stdio.h>
int main()
{
    int *ptr;
    int x=9;
    ptr=&x;
    
    *ptr=8;
    
    printf("value of x is : %d", x); // 8
    return 0;
}  
```

<br>

# 
---
**Sources:**
- [C Dereference Pointer - javatpoint](https://www.javatpoint.com/c-dereference-pointer)