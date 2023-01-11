---
title: C++references
creation-date: 2023-01-10
aliases:
tags:
- CPP/Lecture
- CPP/References
---
**[[C++|HOME [C++]]]**

---
# References
is an alias for another variable. It must therefore be initialized with one the moment it is constructed. It is not possible to make it alias another variable after that.

```cpp
#include <iostream>

int main()
{
    int value1_int{45};
    double value2_double{33.65};

    // int &reference_foo; ERROR!
    int &reference_to_value1_int_1{value1_int};  // throught uniforma initialization
    int &reference_to_value1_int_2 = value1_int; // throught assignment initialization
    double &reference_to_value2_double_1{value2_double};

	reference_to_value1_int_1 = 150;

    std::cout << "value1_int: " << value1_int << std::endl;
    std::cout << "value2_double: " << value2_double << std::endl;
    std::cout << "reference_to_value1_int_1: " << reference_to_value1_int_1 << std::endl;
    std::cout << "reference_to_value1_int_2: " << reference_to_value1_int_2 << std::endl;
    std::cout << "reference_to_value2_double_1: " << reference_to_value2_double_1 << std::endl;
    std::cout << std::endl;
    std::cout << "&value1_int: " << &value1_int << std::endl;
    std::cout << "&value2_double: " << &value2_double << std::endl;
    std::cout << "&reference_to_value1_int_1: " << &reference_to_value1_int_1 << std::endl;
    std::cout << "&reference_to_value1_int_2: " << &reference_to_value1_int_2 << std::endl;
    std::cout << "&reference_to_value2_double_1: " << &reference_to_value2_double_1 << std::endl;
    std::cout << std::endl;
    std::cout << "sizeof(int): " << sizeof(value1_int) << std::endl;
    std::cout << "sizeof(int &): " << sizeof(int &) << std::endl;
    std::cout << "sizeof(reference_to_value1_int_1): " << sizeof(reference_to_value1_int_1) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/book/intro/reference