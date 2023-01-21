---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/template
- CPP/Library/concepts
---
**[[C++|HOME [C++]]]**

---
## Concepts: Logical combinations
concepts can be combined with the logical operators `&&` and `||`
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept tinyType = requires(T t) {
                       sizeof(T) <= 4;
                       requires sizeof(T) <= 4;
                   };

template <typename T>
// T func(T t) require s std::integral<T> || std::floating_point<T>
// T func(T t) require s std::integral<T> && tinyType<T>
T func(T t)
requires std::integral<T> && requires(T T) {
    sizeof(T) <= 4;
    requires sizeof(T) <= 4;
}
```

**e.g.**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept tinyType = requires(T t) {
                       sizeof(T) <= 4;          // simple requirement
                       requires sizeof(T) <= 4; // nested requirement
                   };

template <typename T>
// requires std::integral<T> || std::floating_point<T>
    requires std::integral<T> && tinyType<T>
T add(T a, T b) {
    return (a + b);
}

int main(int argc, char **argv) {
    double var1{6}, var2{10};

    std::cout << add(var1, var2);

    return 0;
}
```