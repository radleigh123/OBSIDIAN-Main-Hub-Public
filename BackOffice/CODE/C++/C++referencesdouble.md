---
aliases:
tags:
- CPP/Lecture
- CPP/References/Double
---
**[[C++|HOME [C++]]]**

---
## Double reference (or rvalue reference)
An [[Cleftrightvalue|rvalue]] reference can bind to a temporary object, which can be moved instead of copied. This can improve performance by avoiding unnecessary memory allocation and deallocation.
**e.g.**
```cpp
#include <iostream>

int main() {
    int num1{150}; // num1 is an lvalue
    int &ref1{num1};
    int &&ref2{num1 + 50}; // &&ref2 is an rvalue

    std::cout << "address of num1: " << &num1 << "  value: " << num1 << std::endl; // 150

    ref1 = 500;

    std::cout << "address of &ref1: " << &ref1 << "  value: " << ref1 << std::endl; // 500
    
    // ref2 is referring to temporary object that no longer exists
    std::cout << "address of &ref2: " << &ref2 << "  value: " << ref2 << std::endl; // 200

    return 0;
}
```
>[!INFO|alt-co clean no-i collapse] **output:**
> address of num1: 0xacf47ffa4c  &nbsp value: 150
> address of &ref1: 0xacf47ffa4c  &nbsp value: 500
> address of &ref2: 0xacf47ffa48  &nbsp value: 200