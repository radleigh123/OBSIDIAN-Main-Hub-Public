---
aliases:
tags:
- CPP/Lecture
- CPP/Operators
---
**[[C++|HOME [C++]]]**

---
## Prefix/Postfix + & -
```cpp
#include <iostream>

int main()
{
    int num1{5};
    std::cout << ++num1 << std::endl; // prefix increment
    std::cout << num1++ << std::endl; // postfix increment

    int num2{10};
    std::cout << --num2 << std::endl; // prefix decrement
    std::cout << num2-- << std::endl; // postfix decrement

    return 0;
}
```