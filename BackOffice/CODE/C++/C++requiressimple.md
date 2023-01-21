---
aliases:
tags:
- CPP/Lecture
- CPP/requires
- CPP/Library/concepts
---
**[[C++requires|BACK]]**

---
## `requires`: simple requirement
expressions only checked for valid syntax
```cpp
template <typename T>
concept tinyType = requires(T t) {
	sizeof(T) <= 4; // simple requirement
};
```
<br>

---
**`double` still valid, despite its size**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept tinyType = requires(T t) { sizeof(T) <= 4; };

tinyType auto add(tinyType auto a, tinyType auto b) { return (a + b); }

int main(int argc, char **argv) {
    double var1{67}, var2{69};

    std::cout << add(var1, var2);
    return 0;
}
```