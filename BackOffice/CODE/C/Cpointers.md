---
title: Pointers
creation-date: 2022-10-26
aliases:
---
**tags:** #C/Pointers 
**[[C|HOME [C]]]**

---
# Pointers
```C
#include<stdio.h>
int main(){
    int num1 = 1025;
    int *ptr;
    ptr = &num1;

    printf("\tAddress of pointer: %p\n", &ptr);
    printf("Size of integer is %d bytes!\n", sizeof(int));

    printf("Address = %p || Value: %d\n", ptr, *ptr); // dereferencing pointer by using '*'

    char *charptr;
    charptr = (char*)ptr; // typecasting

    printf("\n\tAddress of charpointer: %p\n", &charptr);
    printf("Size of character is %d byte!\n", sizeof(char));
    
    printf("Address = %p || Value: %d", charptr, *charptr);
    // 00000000 00000000 00000100 00000001 = every 8bit is 1byte
    // Decimal in Binary/two's complement - explains why value of charptr is 1

    return 0;
}
```

**[Pointer Functions](CPOINTERSfunction.md)** ^459955