---
title: C++dynamiccast
creation-date: 2023-01-30
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/Class/Inheritance
- CPP/virtual/destructors
- CPP/Conversion/dynamic_cast
---
**[[C++|HOME [C++]]]**

---
# Dynamic_cast <>
safely converts pointers and references to classes up, down, and sideways along the inheritance hierarchy. **Syntax:**
```cpp
dynamic_cast <new-type> ( expression )
```
>[!INFO|clean no-t alt-co]
>- transforming from *Base class* pointer/reference to *Derived class* pointer/reference at run time
>- makes it possible to call non polymorphic methods on derived objects

<br>

**dynamic_cast** checks the type of the object at runtime and returns a null pointer if the object is not of the requested type.
```cpp
class Shape {};
class Circle : public Shape {};
class Square : public Shape {};

Shape *shape = new Circle;
Circle *circle = dynamic_cast<Circle*>(shape);

if (circle) // The cast was successful, and you can now access members of Circle
else // The cast failed because shape does not point to a Circle
```
**e.g.**
- [[C++dynamiccastsample0|Simple example]]
- [[C++dynamiccastsample1|Simple example w/ pointers/references]]

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/dynamic_cast