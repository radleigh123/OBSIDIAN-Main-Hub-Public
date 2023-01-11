---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cctype/islower
- CPP/Library/cctype/isupper
---
**[[C++|HOME [C++]]]**

---
## `islower()` `isupper()`
**islower** - checks if the given character is classified as a lowercase character (abcdefghijklmnopqrstuvwxyz).
**isupper** - checks if the given character is an uppercase character (ABCDEFGHIJKLMNOPQRSTUVWXYZ).

```cpp
#include <iostream>

int main() {
    char foo[]{"The C++ Programming is very hard"};
    int lowercase_count{};
    int uppercase_count{};

    std::cout << "foo: " << foo << std::endl;

    // Won't recognize character that aren't alphabetic
    for (auto &character : foo) {
        if (std::islower(character)) {
            std::cout << character << " ";
            lowercase_count++;
        }

        if (std::isupper(character)) {
            std::cout << character << " ";
            uppercase_count++;
        }
    }
    std::cout << std::endl;
    std::cout << "lowercase total: " << lowercase_count << std::endl;
    std::cout << "uppercase total: " << uppercase_count << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/byte/islower
- https://en.cppreference.com/w/cpp/string/byte/isupper