---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/template
- CPP/Conversion
---
**[[C++|HOME [C++]]]**

---
## Template type deduction & Explicit arguments
```cpp
#include <iostream>
template <typename T> T maximum(T var1, T var2);

int main(int argc, char **argv) {
    int a{10}, b{23};
    double c{34.6}, d{23.4};
    std::string e{"Hello"}, f{" World"};

    maximum(a, b); // must be of same type, else ERROR!
    maximum(c, d);
    maximum(e, f);

    maximum<double>(c, d); // solution for different type
    maximum<double>(a, c);
    maximum<double>(a, e); // Error: can't convert string to double

    return 0;
}

template <typename T> T maximum(T var1, T var2) {
    return (var1 > var2) ? var1 : var2;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/function_template