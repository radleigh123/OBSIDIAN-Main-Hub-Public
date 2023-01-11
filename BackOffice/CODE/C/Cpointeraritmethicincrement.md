---
aliases:
tags:
- C/Lecture
- C/Pointers/Arithmetic
---
**[[Cpointerarithmetic|BACK]]**

---
## Incrementing Pointer
>[!column|no-t]
>>[!INFO|clean no-i collapse no-t]
>> The Rule to increment the pointer is:
>> `new_address= address + i * size_of(data type)`
>
>>[!INFO|clean no-i collapse no-t txt-c]
>> For 32-bit `int` variable, it will be incremented by <u>2 bytes</u>
>> For 64-bit `int` variable, it will be incremented by <u>4 bytes</u>

```C
#include<stdio.h>

int main ()
{
    int arr[5] = {1, 2, 3, 4, 5};
    int *p = arr;
    int i;

    printf("printing array elements...\n");
    for(i = 0; i< 5; i++) printf("%d  ",*(p+i));

    return 0;
}
```