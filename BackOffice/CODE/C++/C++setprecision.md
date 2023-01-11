---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/setprecision
---
**[[C++outputformatting|BACK]]**

---
## `setprecision()`
changes floating-point precision

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    double var1{3.1415926535897932238426433827985};

    std::cout << "var1(default precision(6)): " << var1 << std::endl;
    std::cout << std::setprecision(10);
    std::cout << "var1(precision(10)): " << var1 << std::endl;
    std::cout << std::setprecision(20);
    std::cout << "var1(precision(20)): " << var1 << std::endl;

    return 0;
}
```