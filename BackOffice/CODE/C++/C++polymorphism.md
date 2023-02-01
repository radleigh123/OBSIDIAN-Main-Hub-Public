---
title: C++polymorphism
creation-date: 2023-01-26
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
---
**[[C++|HOME [C++]]]**

---
# Polymorphism
a feature that allows a single function or method to work with different types of data, or "polymorphs".
**simplified example:**
```cpp
#include <iostream>

class Base {
public:
  int x;
};

class Derived : public Base {
public:
  int y;
};

int main() {
  Derived d; // since Derived is from Base
  d.x = 10;
  d.y = 20;

  Base *b = &d;
  std::cout << "Value of x through b: " << b->x << std::endl; // 10
  
  // std::cout << "Value of y through b: " << b->y << std::endl;
  // The following line would result in a compile-time error because the member 'y' is not defined in the Base class.

  return 0;
}
```

**e.g.**
[[C++polymorphismsample0|Basic sample]]
[[C++polymorphismsample1|Basic sample using vector]]
[[C++polymorphismsample2|Differences between static and dynamic binding]]
[[C++polymorphismsample3|Static binding with base class pointer/reference]] 

<br>

# 
---
**Sources:**
- https://en.cppreference.com/book/intro/polymorphism
- **virtual function** - https://en.cppreference.com/w/cpp/language/virtual
- **virtual derived class** - https://en.cppreference.com/w/cpp/language/derived_class