---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/boolalpha
---
**[[C++|HOME [C++]]]**

---
## Booleans
```cpp
#include <iostream>

int main()
{
    std::cout << "sizeof(bool): " << sizeof(bool) << std::endl;
    std::cout << "---------------" << std::endl;

    bool green_light{true};
    bool red_light{false};
    std::cout << "green_light: " << green_light << std::endl;
    std::cout << "red_light: " << red_light << std::endl;

    std::cout << std::boolalpha; // changes 0/1 into false/true
    std::cout << "green_light: " << green_light << std::endl;
    std::cout << "red_light: " << red_light << std::endl;

    return 0;
}
```