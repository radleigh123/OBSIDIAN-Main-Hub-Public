---
aliases:
tags:
- CPP/Lecture
- CPP/requires
- CPP/Library/concepts
---
**[[C++requires|BACK]]**

---
## `requires`: Nested requirement
checks if the expression is true

```cpp
template <typename T>
concept tinyType = requires(T t) {
	sizeof(T) <= 4;
	requires sizeof(T) <= 4; // nested requirement
}
```
<br>

---
**Returns false, `double` size higher**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept tinyType = requires(T t) {
                       sizeof(T) <= 4;
                       requires sizeof(T) <= 4;
                   };

tinyType auto add(tinyType auto a, tinyType auto b) { return (a + b); }

int main(int argc, char **argv) {
    double var1{67}, var2{69};

    std::cout << add(var1, var2);

    return 0;
}
```