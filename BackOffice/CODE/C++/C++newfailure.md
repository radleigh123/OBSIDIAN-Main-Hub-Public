---
aliases:
tags:
- CPP/Lecture
- CPP/Expressions/new
- CPP/Pointers
- CPP/Library/exception/exception
- CPP/Library/new/nothrow
---
**[[C++|HOME [C++]]]**

---
## When `new` fails
`new` fails very rarely in practice and you'll see many programs that assume that it always works and don't check for memory allocation failure in any way

**e.g.**
```cpp
#include <iostream>

int main()
{
    // Allocating exceeding array size in one go
    int *ptr_manyints{new int[100000000000000000]};

    // Exhausting memory capabilities of the system
    // When `new` fails, program will forcefully terminate
    for (size_t i = 0; i < 100000000000000000; i++)
        int *ptr_manyints2{new int[100000]};

    return 0;
}
```

>[!TIP|alt-co] Checking for failed memory allocations
>- `std::exception` - if allocation fails, opt for showing some feedback message to the user
> ```cpp
> #include <iostream>
> 
> int main() {
>     for (size_t i = 0; i < 10000000000000; i++)
>     {
>         try
>         {
>             int *ptr_lotsint1{new int[1000000000]};
>         }
>         catch (const std::exception &e)
>         {
>             std::cout << "Caught exception: " << e.what() << std::endl;
>         }
>     }
> 
>     return 0;
> }
> ```
>- `std::nothrow` - ideal if you don't want exceptions thrown when `new` fails
> ```cpp
> #include <iostream>
> 
> int main()
> {
>     for (size_t i = 0; i < 100000000000; i++)
>     {
>         int *ptr_lotsint1{new (std::nothrow) int[10000000000]};
> 
>         if (ptr_lotsint1 == nullptr)
>         {
>             /*
>             Don't try to derefence and use lotsint1 in here
>             You'll get UB. No memory has really been allocated
>             here. It failed and returned nullptr because of the
>             std::nothrow setting
>             */
>             std::cout << "Memory allocation failed" << std::endl;
>             break;
>         }
>         else
>         {
>             std::cout << "Memory allocation succeeded" << std::endl;
>             break;
>         }
>     }
> 
>     return 0;
> }
> ```

<br>

# 
---
**Sources:**
- **exception** - https://en.cppreference.com/w/cpp/error/exception
- **nothrow** - https://en.cppreference.com/w/cpp/memory/new/nothrow
- **try-block** - https://en.cppreference.com/w/cpp/language/try_catch