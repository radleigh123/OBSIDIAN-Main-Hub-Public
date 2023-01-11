---
aliases:
tags:
- C/Lecture
- C/Pointers/Arithmetic
---
**[[Cpointerarithmetic|BACK]]**

---
## Pointer Addition
>[!column|no-t]
>>[!INFO|clean no-i collapse no-t]
>> The Rule to increment the pointer is:
>> `new_address= address + (number * size_of(data type))`
>
>>[!INFO|clean no-i collapse no-t txt-c]
>> For 32-bit `int` variable, it will add <u>2 \* number</u>
>> For 64-bit `int` variable, it will add <u>4 \* number</u>

```C
#include<stdio.h>

int main(){
    int number=50;
    int *p;//pointer to int

    p=&number;//stores the address of number variable     
    printf("Address of p variable is %u \n",p);
    
    p=p+3;   //adding 3 to pointer variable
    printf("After adding 3: Address of p variable is %u \n",p);

    return 0;
}
```