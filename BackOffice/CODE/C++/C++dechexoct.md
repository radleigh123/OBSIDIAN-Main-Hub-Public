---
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/dec
- CPP/Library/io/hex
- CPP/Library/io/oct
---
**[[C++outputformatting|BACK]]**

---
## `std::dec` `std::hex` `std::oct`
changes the base used for integer I/O

```cpp
#include <iostream>
#include <iomanip>

int main()
{
    int pos_int{12345};
    int neg_int{-12345};
    double pos_double{132.45};

    std::cout << "Default base format" << std::endl;
    std::cout << "Positive integer: " << pos_int << std::endl;
    std::cout << "Negative integer: " << neg_int << std::endl;
    std::cout << "Positive double: " << pos_double << std::endl;

    std::cout << std::endl;
    std::cout << "Decimal base format" << std::endl;
    std::cout << "Positive integer: " << std::dec << pos_int << std::endl;
    std::cout << "Negative integer: " << std::dec << neg_int << std::endl;
    
    // does not affect floating-point values
    std::cout << "Positive double: " << std::dec << pos_double << std::endl;

    std::cout << std::endl;
    std::cout << "Hexadecimal base format" << std::endl;
    std::cout << "Positive integer: " << std::hex << pos_int << std::endl;
    std::cout << "Negative integer: " << std::hex << neg_int << std::endl;
    
    // does not affect floating-point values
    std::cout << "Positive double: " << std::hex << pos_double << std::endl;

    std::cout << std::endl;
    std::cout << "Octal base format" << std::endl;
    std::cout << "Positive integer: " << std::oct << pos_int << std::endl;
    std::cout << "Negative integer: " << std::oct << neg_int << std::endl;
    
    // does not affect floating-point values
    std::cout << "Positive double: " << std::oct << pos_double << std::endl;

    return 0;
}
```