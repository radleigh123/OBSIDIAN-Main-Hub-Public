---
aliases:
tags:
- CPP/Lecture
- CPP/Arrays
---
**[[C++|HOME [C++]]]**

---
## Bounds of an [[C++arrays|array]]
```cpp
#include <iostream>

int main()
{
    int arr1[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

    // Read beyond bounds: Will read garbage or crash your program
    std::cout << "arr1[12]: " << arr1[12] << std::endl;

    // Write beyond bounds. The compiler allows it but you don't own the memory at index12, so other programs may modify it and your program may read bogus data at a later time. Or you can even corrupt data used by other parts of your program
    arr1[12] = 25;

    std::cout << "arr1[12]: " << arr1[12] << std::endl;
    return 0;
}
```