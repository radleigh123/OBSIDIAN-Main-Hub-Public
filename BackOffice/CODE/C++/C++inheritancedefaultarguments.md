---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Default Argument Constructors With Inheritance
>[!INFO|clean justified no-t alt-co]
> \- default argument constructors are constructors that take default values for one or more of its arguments. These default values are specified in the constructor's parameter list and are used when the corresponding arguments are not supplied when the constructor is called.

> Always provide a default constructor for your classes, especially if they will be part of an inheritance hierarchy

**e.g.**
```cpp
class baseClassA {
  public:
    baseClassA(int a) {};
};

class baseClassB : public baseClassA {
  public:
    baseClassB(int a, int b) : baseClassA(a) {};
};

class derivedClass : public baseClassB {
  public:
    derivedClass(int a = 0, int b = 0, int c = 0) : baseClassB(a, b) {};
};
```