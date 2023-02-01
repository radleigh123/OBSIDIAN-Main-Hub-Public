---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor
- CPP/Class/Destructor
---
**[[C++|HOME [C++]]]**

---
## Inheritance with destructors
The main reason is that the destructor of a derived class should only deallocate memory and resources that were allocated by the derived class itself, and not the base class.
```cpp
class Base {
public:
    ~Base() { /* some code */ }
};

class Derived : public Base {
public:
    using Base::~Base;
};
```

>[!WARNING|alt-co]+
> inheriting destructors is not a common practice and is not recommended, because it's better to define the destructor explicitly in the derived class, taking into account the specific requirements of the program and the design of the class hierarchy.