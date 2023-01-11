---
aliases:
tags:
- C/Lecture
- C/Pointers
---
**[[C|HOME [C]]]**

---
## Pointer Constant
a constant pointer is pointing to some variable, then it cannot point to any other variable.
**Syntax:** `<type of pointer> *const <name of pointer>;`
```C
#include <stdio.h>

int main()
{
    int a=1;
    int b=2;
    int *const ptr; // constant pointer declaration

    ptr=&a; // ERROR: READ-ONLY VARIABLE `ptr`
    ptr=&b; // ERROR: READ-ONLY VARIABLE `ptr`
    
    printf("Value of ptr is :%d",*ptr);
    return 0;
}
```

### Pointer to Constant
The address of these pointers can be changed, but the value of the variable that the pointer points cannot be changed.
**Syntax:** `const <type of pointer>* <name of pointer>`
```C
#include <stdio.h>
int main()
{
    int a = 100;
    int b = 200;
    const int *ptr; // declaration pointer to constant

    ptr = &b;
    *ptr = 150; // ERROR: ASSIGNMENT OF READ-ONLY LOCATION `ptr`
    
    printf("Value of ptr is :%d", *ptr); // `b = 150` will work
    return 0;
}
```

### Constant Pointer to a Constant
It can neither change the address of the variable to which it is pointing nor it can change the value placed at this address.
**Syntax:** `const <type of pointer>* const <name of the pointer>;`
```C
#include <stdio.h>

int main()
{
    int a = 10;
    int b = 90;
    const int *const ptr = &a;

    ptr = &b; // ERROR: READ-ONLY VARIABLE `ptr`
    *ptr = 12; // ERROR: ASSIGNMENT OF READ-ONLY LOCATION `ptr`

    printf("Value of ptr is :%d", *ptr);
    return 0;
}
```

<br>

# 
---
**Sources:**
- [const Pointer in C - javatpoint](https://www.javatpoint.com/const-pointer-in-c)