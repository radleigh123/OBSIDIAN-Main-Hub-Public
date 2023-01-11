---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strlen
---
**[[C++|HOME [C++]]]**

---
## `strlen()` function
Returns the length of the given byte string, that is, the number of characters in a character array whose first element is pointed to by `str` up to and not including the first null character.
**Syntax:**
```cpp
std::size_t strlen(const char* str);
```
- `str` - pointer to the null-terminated byte string to be examined


```cpp
#include <iostream>
#include <cstring>

int main() {
    const char str1[]{"The sky is blue"};
    const char *ptr_str{"The sky is blue"}; // array decays into pointers when use const char*

    std::cout << "str1: " << str1 << std::endl;

    // strlen() ignores the null character
    std::cout << "strlen(str1): " << std::strlen(str1) << std::endl;
    std::cout << "sizeof(str1): " << sizeof(str1) << std::endl;

    // strlen() still works on decayed array
    std::cout << "\nstrlen(ptr_str): " << std::strlen(ptr_str) << std::endl;
    std::cout << "sizeof(ptr_str): " << sizeof(ptr_str) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strlen