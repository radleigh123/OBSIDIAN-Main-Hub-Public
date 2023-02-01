---
cssclass: bl-c
aliases:
tags:
- CPP/Lecture
- CPP/Pointers/Double
- CPP/Pointers/unique_ptr
- CPP/Pointers/shared_ptr
- CPP/Library/vector/vector
---
**[[C++|HOME [C++]]]**

---
## Pointer to pointer
is a variable that stores the address of another pointer variable.

>[!CHECK|alt-co]+ 
> the standard template library (STL) provides several containers that can be used instead of pointer to pointer:
>>[!column|no-t collapse alt-co flex]
>>>[!INFO|clean no-t collapse]
>>> std::vector
>>> std::list
>>> std::map
>>> std::set
>>
>>>[!INFO|clean no-i collapse] Smart pointers
>>> std::unique_ptr
>>> std::shared_ptr

**e.g.**
```cpp
#include <iostream>

int main()
{
    int num1{150};
    int *ptr1{&num1};
    int **ptr2{&ptr1};

    std::cout << "num1: " << num1 << std::endl;
    std::cout << "*ptr1: " << *ptr1 << std::endl;
    std::cout << "**ptr2: " << **ptr2 << std::endl;

    return 0;
}
```