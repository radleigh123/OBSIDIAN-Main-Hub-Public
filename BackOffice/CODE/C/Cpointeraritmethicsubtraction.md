---
aliases:
tags:
- C/Lecture
- C/Pointers/Arithmetic
---
**[[Cpointerarithmetic|BACK]]**

---
## Pointer Subtraction
>[!column|no-t]
>>[!INFO|clean no-i collapse no-t]
>> The Rule to increment the pointer is:
>> `new_address= address - (number * size_of(data type))`
>
>>[!INFO|clean no-i collapse no-t txt-c]
>> For 32-bit `int` variable, it will subtract <u>2 \* number</u>
>> For 64-bit `int` variable, it will subtract <u>4 \* number</u>

**If two pointers are of the same type,**
`Address2 - Address1 = (Subtraction of two addresses)/size of data type which pointer points`
```C
#include<stdio.h>

void main ()
{
    int i = 100; 
    int *p = &i;
    int *temp;
    temp = p; 
    p = p + 3;
    
    printf("Pointer Subtraction: %d - %d = %d",p, temp, p-temp);
}
```