---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/tolower
- CPP/Library/cctype/toupper
---
**[[C++|HOME [C++]]]**

---
## `tolower()` `toupper()`
**tolower()** - converts a character to lowercase
**toupper()** - converts a character to uppercase

```cpp
#include <iostream>

int main() {
    char str1[]{"Home. the feeling of belonging"};
    char str2[std::size(str1)];

    // Converting to UPPERCASE
    for (size_t i = 0; i < std::size(str1); i++) { str2[i] = std::toupper(str1[i]); }
    std::cout << "str1: " << str1 << std::endl;
    std::cout << "str2: " << str2 << std::endl;

    // Converting to lowercase
    for (size_t i = 0; i < std::size(str1); i++) { str2[i] = std::tolower(str1[i]); }
    std::cout << "\nstr1: " << str1 << std::endl;
    std::cout << "str2: " << str2 << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/tolower
- https://en.cppreference.com/w/cpp/string/byte/toupper