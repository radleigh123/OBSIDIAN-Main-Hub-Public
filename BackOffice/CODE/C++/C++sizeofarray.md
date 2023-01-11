---
aliases:
tags:
- CPP/Lecture
- CPP/Arrays
- CPP/size
---
**[[C++|HOME [C++]]]**

---
## Size of an [[C++arrays|array]]
returns the size of the given range

```cpp
#include <iostream>

int main()
{
    int arr1[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    std::cout << "arr1 size: " << std::size(arr1) << std::endl;

    for (int i = 0; i < std::size(arr1); i++)
    {
        std::cout << "arr1[" << i << "]: " << arr1[i] << std::endl;
    }

    return 0;
}
```

>[!FAQ|alt-co] Longer alternative
> `auto array_size {sizeof(arr1) / sizeof(arr1[0])};`

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/iterator/size