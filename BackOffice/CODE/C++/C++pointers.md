---
title: C++pointers
creation-date: 2023-01-09
aliases:
tags:
- CPP/Lecture
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
# Pointers
**Syntax:** `type *variable_name;`
```cpp
#include <iostream>

int main()
{
    // Explicitely initialize pointers to `nullptr`
    int *int_ptr{};
    double *double_ptr{};
    
    int int_var1{43};
    double double_var1{12.456};
	
	// Declaring pointers to addresses
    int_ptr = &int_var1;
    double_ptr = &double_var1;

    std::cout << "int_var1: " << *int_ptr << std::endl;
    std::cout << "int_ptr (Address in memory): " << int_ptr << std::endl;

	// -----------------------------------------------------
    int int_var2{120};
    int_ptr = &int_var2; // Assign new address to pointer

    std::cout << "\nint_var2: " << *int_ptr << std::endl;
    std::cout << "int_ptr (w/ int_var2 address in memory): " << int_ptr;
    return 0;
}
```
>[!WARNING|alt-co]+ Can't cross assign between pointers of different types
> ```cpp
> int *int_ptr{nullptr};
> double double_var{33};
> 
> int_ptr = &double_var; // COMPILER ERROR
> ```

<br>

# 
---
**Sources:**
- **Pointer** - https://en.cppreference.com/book/pointers
- **Pointer declaration** - https://en.cppreference.com/w/cpp/language/pointer