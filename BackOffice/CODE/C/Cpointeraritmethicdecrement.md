---
aliases:
tags:
- C/Lecture
- C/Pointers/Arithmetic
---
**[[Cpointerarithmetic|BACK]]**

---
## Decrementing Pointer
>[!column|no-t]
>>[!INFO|clean no-i collapse no-t]
>> The Rule to increment the pointer is:
>> `new_address= address - i * size_of(data type)`
>
>>[!INFO|clean no-i collapse no-t txt-c]
>> For 32-bit `int` variable, it will be incremented by <u>2 bytes</u>
>> For 64-bit `int` variable, it will be incremented by <u>4 bytes</u>

```C
#include <stdio.h>

void main(){
    int number=50;
    int *p; //pointer to int

    p=&number; //stores the address of number variable
    printf("Address of p variable is %u \n",p);
    
    p=p-1;
    printf("After decrement: Address of p variable is %u \n",p); // P will now point to the immidiate previous location.
}
```