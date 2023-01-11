---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/showpoint
---
**[[C++outputformatting|BACK]]**

---
## `std::showpoint` `std::noshowpoint`
controls whether decimal point is always included in floating-point representation

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    double var1{34.1}, var2{101.99}, var3{12.0}, var4{45};

    std::cout << "noshowpoint (default): " << std::endl;
    std::cout << "var1: " << var1 << std::endl;
    std::cout << "var2: " << var2 << std::endl;
    std::cout << "var3: " << var3 << std::endl;
    std::cout << "var4: " << var4 << std::endl;

    std::cout << std::endl;
    std::cout << "showpoint: " << std::showpoint << std::endl;
    std::cout << "var1: " << var1 << std::endl;
    std::cout << "var2: " << var2 << std::endl;
    std::cout << "var3: " << var3 << std::endl;
    std::cout << "var4: " << var4 << std::endl;

    return 0;
}
```