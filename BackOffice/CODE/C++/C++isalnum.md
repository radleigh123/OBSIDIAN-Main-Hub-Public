---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/isalnum
---
**[[C++|HOME [C++]]]**

---
## `isalnum()` function
checks if a character is alphanumeric
- digits (0123456789)
- uppercase letters (ABCDEFGHIJKLMNOPQRSTUVWXYZ)
- lowercase letters (abcdefghijklmnopqrstuvwxyz)

**e.g.**
```cpp
#include <iostream>

int main() {
    std::cout << "C is alphanumeric: " << std::isalnum('C') << std::endl;
    std::cout << "^ is alphanumeric: " << std::isalnum('^') << std::endl;
    std::cout << std::endl;

    // Can use this as a test condition
    char input_char{'*'};
    if (std::isalnum(input_char)) std::cout << input_char << " is alphanumeric\n";
    else std::cout << input_char << " is not alphanumeric";

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/isalnum