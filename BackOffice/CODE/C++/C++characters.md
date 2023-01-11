---
title: C++characters
creation-date: 2023-01-07
aliases:
tags:
- CPP/Lecture
- CPP/Conversion/static_cast
---
**[[C++|HOME [C++]]]**

---
# Characters & Text
```cpp
#include <iostream>

int main()
{
    char value{65};

    std::cout << "Value: " << value << std::endl;
    std::cout << "Value(int): " << static_cast<int>(value) << std::endl;

    return 0;
}
```