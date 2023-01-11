---
aliases:
---
**tags:** #C/Pointers 
**[[0Pointers|BACK]]**

---
```C
#include<stdio.h>
int main(){
    int *ptr1, **ptr2, ***ptr3, num1 = 1;
    printf("Original Address ptr1: %p\n", &ptr1);
    printf("Original Address ptr2: %p\n", &ptr2);
    printf("Original Address ptr3: %p\n", &ptr3);
    printf("Original Address num1: %p\n\n", &num1);
    
    ptr1 = &num1;
    printf("Address of ptr1: %p\tValue of ptr1: %d\n", ptr1, *ptr1);

    ptr2 = &ptr1;
    printf("Address of ptr2: %p\tValue of ptr2: %d\n", ptr2, *(*ptr2));

    ptr3 = &ptr2;
    printf("Address of ptr3: %p\tValue of ptr3: %d\n", ptr3, *(*(*ptr3)));

    return 0;
}
```