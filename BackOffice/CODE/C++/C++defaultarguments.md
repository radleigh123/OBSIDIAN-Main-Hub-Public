---
title: C++defaultarguments
creation-date: 2023-01-30
aliases:
tags:
- CPP/Lecture
- CPP/Functions/default
---
**[[C++|HOME [C++]]]**

---
# Default arguments
allows a function to be called without providing one or more trailing arguments.
**e.g.**
```cpp
#include <iostream>

// Declare a function with a default argument
int addNumbers(int a, int b = 50) { return a + b; }

int main() {
    // Call the function with two arguments, the default value of b is not used
    std::cout << "addNumbers(10, 10): " << addNumbers(10, 10) << std::endl;

    // Call the function with one argument, the default value of b is used
    std::cout << "addNumbers(10): " << addNumbers(10) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/default_arguments