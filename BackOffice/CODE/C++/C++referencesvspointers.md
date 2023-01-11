---
cssclass:
- t-c
- tbl-nalt
aliases:
tags:
- CPP/Lecture
- CPP/References
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## References & Pointers
> **references** are somewhat like `const pointers`

<br>

| REFERENCES                                                               | POINTERS                                                             |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| don't use dereferencing for reading/writing                              | must go through dereference operator to read/write                   |
| <mark class="hltr-lightred">can't be changed to reference another</mark> | <mark class="hltr-lightgreen">can be changed to point another</mark> |
| must be initialized at declaration                                       | can be declared un-initialized                                       |

```cpp
#include <iostream>

int main()
{
    auto dob_value{45.666};
    double &ref_dob_value{dob_value};
    double *ptr_dob_value{&dob_value};

    std::cout << "dob_value: " << dob_value << std::endl;
    std::cout << "dob_value address: " << &dob_value << std::endl;
    std::cout << "\nref_dob_value: " << ref_dob_value << std::endl;
    std::cout << "ref_dob_value address: " << &ref_dob_value << std::endl;
    std::cout << "\nptr_dob_value: " << *ptr_dob_value << std::endl;
    std::cout << "ptr_dob_value address: " << ptr_dob_value << std::endl;

    return 0;
}
```