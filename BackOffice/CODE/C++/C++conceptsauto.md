---
aliases:
tags:
- CPP/Lecture
- CPP/Library/concepts
- CPP/auto
---
**[[C++|HOME [C++]]]**

---
## Concepts: `auto`
**e.g.**
```cpp
// This syntax constraints the `auto` parameters you pass into comply with the std::integral concept
std::integral auto add(std::integral auto a, std::integral auto b) {
    return (a + b);
}
```

```cpp
// Constrain declared auto var
std::integral auto x = add(20, 10);
// std::floating_point auto x = add(20, 10); // Compiler error
std::cout << "x: " << x << std::endl;
```

```cpp
// std::integral auto y = 7.7;
std::floating_point auto y = 7.7;
std::cout << "y: " << y << std::endl;
```
<br>

**Returns false, data is not a floating type**
```cpp
#include <iostream>
#include <concepts>

std::integral auto add(std::integral auto a, std::integral auto b) {
    return (a + b);
}

int main(int argc, char **argv) {
    // std::integral auto x{add(10, 40)};
    std::floating_point auto x{add(5, 8)};

    return 0;
}
```