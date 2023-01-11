---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/fixed
- CPP/Library/io/scientific
- CPP/Library/io/hexfloat
- CPP/Library/io/ios_base/unsetf
---
**[[C++outputformatting|BACK]]**

---
## `std::fixed` `std::scientific` `std::hexfloat` `std::defaultfloat`
changes formatting used for floating-point I/O

```cpp
#include <iostream>

int main()
{
    double var1{3.1415926535897932238426433827985};
    double var2{2006.0};
    double var3{1.34e-10};

    std::cout << std::endl;
    std::cout << "double values (default: use scientific where necessary)" << std::endl;
    std::cout << "Variable 1 = " << var1 << std::endl;
    std::cout << "Variable 2 = " << var2 << std::endl;
    std::cout << "Variable 3 = " << var3 << std::endl;

    std::cout << std::endl;
    std::cout << "double values (fixed): " << std::endl;
    std::cout << std::fixed;
    std::cout << "Variable 1 = " << var1 << std::endl;
    std::cout << "Variable 2 = " << var2 << std::endl;
    std::cout << "Variable 3 = " << var3 << std::endl;

    std::cout << std::endl;
    std::cout << "double values (scientific): " << std::endl;
    std::cout << std::scientific;
    std::cout << "Variable 1 = " << var1 << std::endl;
    std::cout << "Variable 2 = " << var2 << std::endl;
    std::cout << "Variable 3 = " << var3 << std::endl;

    std::cout << std::endl;
    std::cout << "double values (back to default): " << std::endl;
    std::cout.unsetf(std::ios::scientific | std::ios::fixed);
    std::cout << "Variable 1 = " << var1 << std::endl;
    std::cout << "Variable 2 = " << var2 << std::endl;
    std::cout << "Variable 3 = " << var3 << std::endl;

    return 0;
}
```