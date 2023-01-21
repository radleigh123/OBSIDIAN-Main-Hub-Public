---
aliases:
tags:
- CPP/Lecture
- CPP/auto
---
**[[C++|HOME [C++]]]**

---
## Auto
lets the compiler deduce the type, automatically identifies the variable

```cpp
#include <iostream>

int main()
{
    auto var1{12};
    auto var2{13.0L};
    auto var3 = {'H', 'e', 'l'};

    // int modifier suffixes
    auto var4{123u};  // unsigned
    auto var5{123ul}; // unsigned long
    auto var6{123ll}; // long long

    return 0;
}
```