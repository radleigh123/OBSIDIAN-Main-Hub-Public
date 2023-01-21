---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strcat
---
**[[C++|HOME [C++]]]**

---
## `strcat` function
Appends a copy of the character string pointed to by `src` to the end of the character string pointed to by `dest`.
**Syntax:**
```cpp
char *strcat( char *dest, const char *src );
```
**dest**	-	pointer to the null-terminated byte string to append to
**src**	-	pointer to the null-terminated byte string to copy from

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main() {
    char dest[50]{"Hello"};
    char src[50]{" World"};

    std::strcat(dest, src);
    std::strcat(dest, " This string will append");

    std::cout << "dest\n" << dest << std::endl;
    return 0;
}
```

**Concatenating with the use of pointers & `new char`**
```cpp
#include <iostream>
#include <cstring>

int main() {
    char *dest1{new char[30]{'F', 'i', 'r', 'e', 'l', 'o', 'r', 'd', '\0'}};
    char *src1{new char[30]{',', 'T', 'h', 'e', ' ', 'P', 'h', 'o', 'e', 'n', 'i', 'x', '\0'}};

    std::cout << "std::strlen(dest1): " << std::strlen(dest1) << std::endl;
    std::cout << "std::strlen(src1): " << std::strlen(src1) << std::endl;

    std::cout << "\nConcatenating..." << std::endl;
    std::strcat(dest1, src1); // does not add the '\0

    std::cout << "std::strlen(dest1): " << std::strlen(dest1) << std::endl;
    std::cout << "dest1: " << dest1 << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strcat