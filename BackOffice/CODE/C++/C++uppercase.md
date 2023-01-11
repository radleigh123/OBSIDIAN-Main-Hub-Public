---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/uppercase
- CPP/Library/io/showbase
---
**[[C++outputformatting|BACK]]**

---
## `std::uppercase` `std::nouppercase`
controls whether uppercase characters are used with some output formats

```cpp
#include <iostream>

int main()
{
    std::cout << std::hex << std::showbase
              << "0x2a w/ uppercase: " << std::uppercase << 0x2a << '\n'
              << "0x2a w/ nouppercase: " << std::nouppercase << 0x2a << '\n'
              << "1e-10 w/ uppercase: " << std::uppercase << 1e-10 << '\n'
              << "1e-10 w/ nouppercase: " << std::nouppercase << 1e-10 << '\n'
              << std::endl;

    return 0;
}
```

>[!WARNING|alt-co] **Has no effect on input**