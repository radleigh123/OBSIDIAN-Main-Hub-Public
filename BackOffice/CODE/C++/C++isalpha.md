---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/isalpha
---
**[[C++|HOME [C++]]]**

---
## `isalpha()` function
Checks if the given character is an alphabetic character as classified by the currently installed C locale.
- uppercase letters (ABCDEFGHIJKLMNOPQRSTUVWXYZ)
- lowercase letters (abcdefghijklmnopqrstuvwxyz)

**e.g.**
```cpp
#include <iostream>

int main() {
    std::cout << "C is alphabetic: " << std::isalpha('C') << std::endl;
    std::cout << "^ is alphabetic: " << std::isalpha('^') << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/isalpha