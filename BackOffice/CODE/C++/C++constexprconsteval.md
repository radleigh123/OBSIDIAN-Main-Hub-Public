---
title: C++constexprconsteval
creation-date: 2023-01-08
aliases:
tags:
- CPP/Lecture
- CPP/constexpr
- CPP/consteval
---
**[[C++|HOME [C++]]]**

---
## `constexpr`
used to create compile-time (symbolic) constants. We also introduced constant expressions, which are expressions that can be evaluated at compile-time rather than runtime.
```cpp
#include <iostream>

constexpr int greater(int x, int y) { // a constexpr function
    return (x > y ? x : y);
}

int main() {
    constexpr int x{5};
    constexpr int y{6};

    constexpr int g{greater(x, y)}; // will be evaluated at compile-time

    std::cout << g << " is greater!\n";

    return 0;
}
```

## `consteval`
which is used to indicate that a function _must_ evaluate at compile-time, otherwise a compile error will result. Such functions are called immediate functions.
```cpp
#include <iostream>

consteval int greater(int x, int y) // function is now consteval
{
    return (x > y ? x : y);
}

int main()
{
    constexpr int g { greater(5, 6) };            // ok: will evaluate at compile-time
    std::cout << greater(5, 6) << " is greater!\n"; // ok: will evaluate at compile-time

    int x{ 5 }; // not constexpr
    std::cout << greater(x, 6) << " is greater!\n"; // error: consteval functions must evaluate at compile-time

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://www.learncpp.com/cpp-tutorial/constexpr-and-consteval-functions/
- https://en.cppreference.com/w/cpp/language/constexpr
- https://en.cppreference.com/w/cpp/language/consteval