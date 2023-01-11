---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strncmp
---
**[[C++|HOME [C++]]]**

---
## `strncmp()` function
Compares at most `count` characters of two possibly null-terminated arrays.
**Syntax:**
```cpp
int strncmp( const char *lhs, const char *rhs, std::size_t count );
```
- `lhs` `rhs` - pointers to the possibly null-terminated arrays to compare
- `count` - maximum number of characters to compare

```cpp
#include <iostream>
#include <cstring>

int main() {
    const char *str1{"alabama"};
    const char *str2{"blabama"};
    size_t var1{3};
    std::cout << "strncmp(" << str1 << ", " << str2 << ", " << var1 << ") : " << std::strncmp(str1, str2, var1) << std::endl;

    str1 = "clabama";
    str2 = "blabama";
    std::cout << "strncmp(" << str1 << ", " << str2 << ", " << var1 << ") : " << std::strncmp(str1, str2, var1) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strncmp