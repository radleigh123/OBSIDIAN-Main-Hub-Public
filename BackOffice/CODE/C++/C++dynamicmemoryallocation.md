---
aliases:
tags:
- CPP/Lecture
- CPP/Memory
- CPP/Expressions/delete
- CPP/Expressions/new
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## Dynamic Memory Allocation
**delete expression** - destroys object(s) previously allocated by the new expression and releases obtained memory area.
Syntax:
- `delete expression`
- `delete []expression`

**e.g.**
```cpp
#include <iostream>

int main()
{
    // Initializing pointers with a valid address on declaration. Not with `nullptr`
    int *ptr_var1{new int};     // junk value
    int *ptr_var2{new int(22)}; // direct initialization
    int *ptr_var3{new int{25}}; // uniform initialization

    std::cout << "Initialize w/ valid memory address at declaration" << std::endl;
    std::cout << "ptr_var1: " << ptr_var1 << "  - junk values" << std::endl;
    std::cout << "ptr_var1: " << *ptr_var1 << "  - junk values" << std::endl;

    std::cout << "\nptr_var2: " << ptr_var2 << std::endl;
    std::cout << "ptr_var2: " << *ptr_var2 << std::endl;

    std::cout << "\nptr_var3: " << ptr_var3 << std::endl;
    std::cout << "ptr_var3: " << *ptr_var3 << std::endl;

    // Remember to release the memory
    delete ptr_var1;
    ptr_var1 = nullptr; // To play it safe

    delete ptr_var2;
    ptr_var2 = nullptr;

    delete ptr_var3;
    ptr_var3 = nullptr;

    return 0;
}
```

**new expression** - Creates and initializes objects with dynamic storage duration, that is, objects whose lifetime is not necessarily limited by the scope in which they were created.
Syntax:
- `new (type) initializer`(optional)
- `new new-type initializer`(optional)
- `new (placement-params) (type) initializer`(optional)
- `new (placement-params) new-type initializer`(optional)

**e.g.**
```cpp
#include <iostream>

int main()
{
    // Dynamic heap memory
    int *ptr_var1{nullptr};
    ptr_var1 = new int;
    /*
    Dynamically allocate space for a single int on the heap. This
    memory belongs to our program from now on. The system can;t use
    it for anything else, until we return it. After this line executes,
    we will have a valid memory location allocated. The size of the
    allocated memory will be such that it can store the type pointed
    to by the pointer
    */

    *ptr_var1 = 77; // Writing into dynamically allocated memory
    std::cout << "Dynamically allocating memory\n";
    std::cout << "ptr_var1: " << *ptr_var1 << std::endl;

	delete ptr_var1; // ptr_var1 will now contain junk
    ptr_var1 = nullptr;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/delete