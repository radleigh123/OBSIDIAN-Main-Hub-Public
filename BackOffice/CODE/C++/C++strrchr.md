---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strrchr
---
**[[C++|HOME [C++]]]**

---
## `strrchr()` function
Finds the last occurrence of `ch` (after conversion to char) in the byte string pointed to by str.
**Syntax:**
```cpp
const char *strrchr( const char* str, int ch );
char *strrchr(char* str, int ch );
```
- `str` - pointer to the null-terminated byte string to be analyzed
- `ch` - character to search for

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main()
{
    char input[]{"/home/user/hello.cpp"};
    char *output{std::strrchr(input, '/')};

    if (output)
    {
        // +1 becuase we want to start printing past the character found by strrchr()
        std::cout << output + 1 << std::endl;
    }

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strrchr