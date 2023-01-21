---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strcpy
---
**[[C++|HOME [C++]]]**

---
## `strcpy` function
Copies the character string pointed to by `src`, including the null terminator, to the character array whose first element is pointed to by `dest`.
**Syntax:**
```cpp
char* strcpy( char* dest, const char* src );
```
**dest**	-	pointer to the character array to write to
**src**	-	pointer to the null-terminated byte string to copy from

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main() {
    const char *src{"C++ is a multipurpose language"};
    // +1 for '\0', strlen does not include null
    char *dest{new char[std::strlen(src) + 1]};

    std::strcpy(dest, src);

    std::cout << "sizeof(dest): " << sizeof(dest) << std::endl;
    std::cout << "strlen(dest): " << std::strlen(dest) << std::endl;
    std::cout << "dest: " << dest << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strcpy