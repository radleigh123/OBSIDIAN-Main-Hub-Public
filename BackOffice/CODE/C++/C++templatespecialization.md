---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/template
- CPP/Functions/template/specialization
- CPP/Library/stringh/strcmp
- CPP/Library/cstring/strcmp
---
**[[C++|HOME [C++]]]**

---
## Template specialization
```cpp
#include <iostream>
#include <string.h>

// Function template
template <typename T>
T maximum(T var1, T var2);

// Function specialization
template <>
const char *maximum<const char *>(const char *a, const char *b);

int main(int argc, char **argv) {
    int a{10}, b{25};
    double c{45.33}, d{88.33};
    std::string e{"hello"}, f{" world"};

    int max_int;
    double max_double;
    std::string max_str;

    // compiler will prefer to use function specialization
    const char *g{"spider"};
    const char *h{"man"};

    std::cout << "max(const char *): " << maximum(g, h) << std::endl;
    return 0;
}

template <typename T>
T maximum(T var1, T var2) {
    return (var1 > var2) ? var1 : var2;
}

template <>
const char *maximum<const char *>(const char *a, const char *b) {
    return (strcmp(a, b) > 0) ? a : b;
}
```