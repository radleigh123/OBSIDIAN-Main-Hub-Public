---
title: C++functionslambdacapturelists
creation-date: 2023-01-13
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
- CPP/References
---
**[[C++|HOME [C++]]]**

---
# Capture Lists
**Capturing by value**
```cpp
#include <iostream>

int main(int argc, char **argv) {
    int c{42};
    auto func = [c](){
        std::cout << "Inner value: " << c << std::endl;
    };

    for (size_t i = 0; i < 3; i++) {
        std::cout << "\nOuter value: " << c << std::endl;
        func();
        c++;
    }

    return 0;
}
```

**Capture by reference**
```cpp
#include <iostream>

int main(int argc, char **argv) {
    int c{42};
    auto func = [&c](){
        std::cout << "Inner value: " << c << std::endl;
    };

    for (size_t i = 0; i < 5; i++) {
        std::cout << "\nOuter value: " << c << std::endl;
        func();
        c++;
    }

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/lambda