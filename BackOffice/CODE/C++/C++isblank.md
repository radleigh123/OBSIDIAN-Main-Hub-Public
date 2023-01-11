---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/isblank
---
**[[C++|HOME [C++]]]**

---
## `isblank()` function
checks if a character is a blank character

```cpp
#include <iostream>

int main() {
    char message[]{"Hello World. How are you?"};
    int blank_count{};

    for (size_t i = 0; i < std::size(message); i++) {
        if (std::isblank(message[i])) {
            std::cout << "Found a blank character at index[" << i << "]\n";
            blank_count++;
        }
    }
    
    std::cout << "\nTotal: " << blank_count << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/isblank