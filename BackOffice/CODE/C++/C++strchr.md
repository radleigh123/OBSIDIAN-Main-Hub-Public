---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cstring/strchr
---
**[[C++|HOME [C++]]]**

---
## `strchr()` function
Finds the first occurrence of the character static_cast<char>(ch) in the byte string pointed to by str.
**Syntax:**
```cpp
const char *strchr(const char *str, int ch);
char *strchr(char *str, int ch);
```
- `str` pointer to the null-terminated byte string to be analyzed
- `ch` character to search for

**e.g.**
```cpp
#include <iostream>
#include <cstring>

int main() {
    const char *str{"Try not. Do, or do not."};
    char target = 'T';
    const char *result{str};
    int count{};

    while ((result = std::strchr(result, target)) != nullptr) {
        std::cout << "Found '" << target << " starting at '" << result << "'\n";

        // Increment result, otherwise we'll find target at the same location
        result++;
        count++;
    }
    std::cout << "Iterations: " << count << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/strchr