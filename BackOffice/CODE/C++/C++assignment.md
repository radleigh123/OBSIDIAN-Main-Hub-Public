---
aliases:
tags:
- CPP/Lecture
- CPP/Operators
---
**[[C++|HOME [C++]]]**

---
## Assignments
```cpp
#include <iostream>

int main()
{
    int var1{12}; // Declaring and Initializing

    var1 = 125; // Assigning

    std::cout << var1 << std::endl;
    return 0;
}
```

>[!WARNING|alt-co]+ Careful on assigning different data types
> ```cpp
> #include <iostream>
> 
> int main()
> {
>     auto var1{150u};
> 
> 	// unsigned integer only stores positive values
>     var1 = -125;
>     
>     std::cout << var1 << std::endl;
>     return 0;
> }
> ```