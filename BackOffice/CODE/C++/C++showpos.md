---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/showpos
---
**[[C++outputformatting|BACK]]**

---
## `std::showpos` `std::noshowpos`
controls whether the `+` sign used with non-negative numbers

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    int num1{10}, num2{-125};

    std::cout << "noshowpos (default)" << std::endl;
    std::cout << "Positive: " << num1 << std::endl;
    std::cout << "Negative: " << num2 << std::endl;

    std::cout << std::endl;
    std::cout << std::showpos << "showpos" << std::endl;
    std::cout << "Positive: " << num1 << std::endl;
    std::cout << "Negative: " << num2 << std::endl;

    return 0;
}
```