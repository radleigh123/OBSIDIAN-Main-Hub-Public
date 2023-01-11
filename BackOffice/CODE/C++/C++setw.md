---
aliases:
tags:
- CPP/Library/io/Manipulators
- CPP/Library/io/setw
- CPP/Library/io/right
- CPP/Library/io/left
- CPP/Library/io/internal
---
**[[C++outputformatting|BACK]]**

---
## `setw()`
changes the width of the next input/output field

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    int first_col{20}, sec_col{20};

    std::cout << "Right Formatted Table (default)" << std::endl;
    std::cout << std::setw(first_col) << "Daniel"
              << std::setw(sec_col) << "Gray"
              << std::setw(sec_col) << " 25"
              << std::endl;
    std::cout << std::setw(first_col) << "Rhiz"
              << std::setw(sec_col) << "Caballero"
              << std::setw(sec_col) << " 98"
              << std::endl;

    std::cout << std::endl;
    std::cout << std::left;
    std::cout << "Left Formatted Table" << std::endl;
    std::cout << std::setw(first_col) << "Daniel"
              << std::setw(sec_col) << "Gray"
              << std::setw(sec_col) << " 25"
              << std::endl;
    std::cout << std::setw(first_col) << "Rhiz"
              << std::setw(sec_col) << "Caballero"
              << std::setw(sec_col) << " 98"
              << std::endl;

    std::cout << std::endl;
    std::cout << std::internal;
    std::cout << "Internal Formatted Table" << std::endl;
    std::cout << std::setw(first_col) << "Daniel"
              << std::setw(sec_col) << "Gray"
              << std::setw(sec_col) << " 25"
              << std::endl;
    std::cout << std::setw(first_col) << "Rhiz"
              << std::setw(sec_col) << "Caballero"
              << std::setw(sec_col) << " 98"
              << std::endl;

    return 0;
}
```