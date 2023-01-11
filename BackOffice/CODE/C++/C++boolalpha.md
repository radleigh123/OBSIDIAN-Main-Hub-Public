---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/boolalpha
---
**[[C++outputformatting|BACK]]**

---
## `std::boolaplha` `std::noboolalpha`
switches between textual and numeric representation of Booleans

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    bool white{1};
    bool black{false};

    std::cout << "noboolalpha (default)" << std::endl;
    std::cout << "White: " << white << std::endl;
    std::cout << "Black: " << black << std::endl;

    std::cout << std::endl;
    std::cout << std::boolalpha;
    std::cout << "boolalpha" << std::endl;
    std::cout << "White: " << white << std::endl;
    std::cout << "Black: " << black << std::endl;

    return 0;
}
```