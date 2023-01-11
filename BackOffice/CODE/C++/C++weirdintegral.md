---
aliases:
tags:
- CPP/Lecture
---
**[[C++|HOME [C++]]]**

---
## Weird Integral types
>[!WARNING|alt-co ttl-c] Integral types less than 4bytes in size don't support arithmetic operations

```cpp
#include <iostream>

int main()
{
    short int var1{10}, var2{20}; // 2bytes
    char var3{40}, var4{50}; // 1byte

    std::cout << "size of var1: " << sizeof(var1) << std::endl;
    std::cout << "size of var2: " << sizeof(var2) << std::endl;
    std::cout << "size of var3: " << sizeof(var3) << std::endl;
    std::cout << "size of var4: " << sizeof(var4) << std::endl;

    auto result1 = var1 + var2; // int conversion
    auto result2 = var3 + var4;

    std::cout << std::endl;
    std::cout << "size of result1: " << sizeof(result1) << std::endl;
    std::cout << "size of result2: " << sizeof(result2) << std::endl;

    return 0;
}
```