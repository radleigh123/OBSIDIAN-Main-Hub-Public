---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/isdigit
---
**[[C++|HOME [C++]]]**

---
## `isdigit()` function
Checks if the given character is one of the 10 decimal digits: 0123456789

```cpp
#include <iostream>

int main() {
    char statement[]{"Hello World, I own 77 lambo and 69 houses."};
    int digit_count{};

    std::cout << "statement: " << statement << std::endl;

    for (auto &character : statement) {
        if (std::isdigit(character)) {
            std::cout << "Found digit: " << character << std::endl;
            digit_count++;
        }
    }

    std::cout << "\nTotal digits found: " << digit_count;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/isdigit