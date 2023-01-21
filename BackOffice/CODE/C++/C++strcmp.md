---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strcmp
- CPP/Library/stringh/strcmp
---
**[[C++|HOME [C++]]]**

---
## `strcmp()` function
Compares two null-terminated byte strings lexicographically.
**Syntax:**
```cpp
int strcmp( const char *lhs, const char *rhs );
```
- `lhs` `rhs` - pointers to the null-terminated byte strings to compare

```cpp
#include <iostream>
#include <cstring>

int main()
{
    const char *str1{"Ala"};
    const char *str2{"Bla"};

    std::cout << "std::strcmp(" << str1 << ", " << str2 << "): " << std::strcmp(str1, str2) << std::endl;

    str1 = "Ala";
    str2 = "Ala";
    std::cout << "std::strcmp(" << str1 << ", " << str2 << "): " << std::strcmp(str1, str2) << std::endl;

    str1 = "Bla";
    str2 = "Ala";
    std::cout << "std::strcmp(" << str1 << ", " << str2 << "): " << std::strcmp(str1, str2) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strcmp