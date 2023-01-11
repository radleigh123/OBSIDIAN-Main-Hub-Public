---
title: C++numbersystems
creation-date: 2023-01-06
aliases:
tags:
- CPP/Lecture
---
**[[C++|HOME [C++]]]**

---
# Number Systems
```cpp
#include <iostream>

int main()
{
    int num1 = 15;         // Decimal
    int num2 = 017;        // Octal of `num1`
    int num3 = 0x0f;       // Hexadecimal of `num1`
    int num4 = 0b00001111; // Binary - C++14 of `num1`

    std::cout << "No.1 = " << num1 << std::endl;
    std::cout << "No.2 = " << num2 << std::endl;
    std::cout << "No.3 = " << num3 << std::endl;
    std::cout << "No.4 = " << num4 << std::endl;

    return 0;
}
```