---
aliases:
tags:
- CPP/Lecture
---
**[[C++|HOME [C++]]]**

---
## First program of C++
```cpp
#include <iostream>

int main()
{
    std::cout << "Hello World" << std::endl;

    return 0;
}
```

---

```cpp
#include <iostream>

int main()
{
    // Compiler syntax error: missing semicolon
    std::cout << "Hello World" << std::endl;

    int a{4}, b{5};

    // Runtime error
    int c = 10 / (a - b);
    std::cout << "The value of c is " << c << std::endl;

    // Warnings
    20 / 0; // This throws a warning on gcc10

    return 0;
}
```