---
aliases:
tags:
- CPP/Lecture
- CPP/References
- CPP/const
---
**[[C++|HOME [C++]]]**

---
## References & `const`
**Non const reference**
```cpp
#include <iostream>

int main() {
    int age{27};
    int &ref_age{age};

    std::cout << "age: " << age << std::endl;
    std::cout << "ref_age: " << ref_age << std::endl;

    ++ref_age; // Can modify original variable through reference
    std::cout << "\nage: " << age << std::endl;
    std::cout << "ref_age: " << ref_age << std::endl;

    return 0;
}
```

**const reference**
```cpp
#include <iostream>

int main() {
    int age{25};
    const int &constref_age{age};

    ++constref_age; // ERROR! Expression must be a modifiable lvalue

    std::cout << "age: " << age << std::endl;
    std::cout << "constref_age: " << constref_age << std::endl;

    return 0;
}
```

>[!NOTE]+ Duplicate const reference behavior w/ pointers
> const ref with pointer : const pointer to const data
> ```cpp
> #include <iostream>
> 
> int main() {
>     int age{15};
>     const int *const const_ptr_to_const_age{&age};
>
>     *constptr_to_const_age = 45; // ERROR!
>
>     return 0;
> }
> ```