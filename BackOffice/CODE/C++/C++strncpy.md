---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strncpy
---
**[[C++|HOME [C++]]]**

---
## `strncpy` function
Copies at most `count` characters of the byte string pointed to by `src` (including the terminating null character) to character array pointed to by `dest`.
**Syntax:**
```cpp
char *strncpy( char *dest, const char *src, std::size_t count );
```
**dest**	-	pointer to the character array to copy to
**src**	-	pointer to the byte string to copy from
**count**	-	maximum number of characters to copy

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main() {
    const char *src{"Hello"};
    // terminating null '\0'  is needed if we want print
    char dest[]{'a', 'b', 'c', 'd', 'e', 'f', 'g', '\0'};

    std::cout << "dest: " << dest << std::endl;
    std::cout << "\nCopying..." << std::endl;
    std::cout << "dest: " << std::strncpy(dest, src, 5) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strncpy