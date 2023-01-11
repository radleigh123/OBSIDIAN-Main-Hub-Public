---
title: C++pointernull
creation-date: 2023-01-10
aliases:
tags:
- CPP/Lecture
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
# Null pointer safety
making sure pointers contain a valid memory address

**Verbose `nullptr` check**
```cpp
#include <iostream>

int main()
{
    int *ptr_var{}; // initialized to nullptr

    if (!(ptr_var == nullptr))
        std::cout << "ptr_var points to a VALID address: " << ptr_var << std::endl;
    else
        std::cout << "ptr_var points to a INVALID address" << std::endl;

    return 0;
}
```

>[!NOTE]+ Calling `delete` on a pointer containing `nullptr`
> ```cpp
> #include <iostream>
> 
> int main() {
>     int *ptr_var1{};
>     
>     delete ptr_var1; // if ptr_var1 contains `nullptr`, won't cause ERROR
> 
>     // Redundant below...
>     /*
>     if (ptr_var1) {
>         delete ptr_var1;
>         ptr_var1 = nullptr;
>     }
>     */
> 
>     return 0;
> }
> ```