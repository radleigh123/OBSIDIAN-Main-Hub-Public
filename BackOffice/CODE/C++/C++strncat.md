---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strncat
---
**[[C++|HOME [C++]]]**

---
## `strncat` function
Appends a byte string pointed to by `src` to a byte string pointed to by `dest`. At most `count` characters are copied.
**Syntax:**
```cpp
char *strncat( char *dest, const char *src, std::size_t count );
```
**dest**	-	pointer to the null-terminated byte string to append to
**src**	-	pointer to the null-terminated byte string to copy from
**count**	-	maximum number of characters to copy

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main() {
    char dest[50]{"Bello"};
    char src[30]{" There is a bird on my rocket"};

    std::strncat(dest, src, 6);
    // for immediate printout
    // std::cout << std::strncat(dest, src, 6) << std::endl;

    std::cout << "The concatenated string: " << dest << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strncat