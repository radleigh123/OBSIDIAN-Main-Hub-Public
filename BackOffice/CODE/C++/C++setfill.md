---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
---
**[[C++outputformatting|BACK]]**

---
## `setfill()`
changes the fill character

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    int first_col{20}, sec_col{20};

    std::cout << std::setfill('-');
    std::cout << "Right Formatted Table (default)" << std::endl;
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