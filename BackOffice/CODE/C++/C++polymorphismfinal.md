---
title: C++polymorphismfinal
creation-date: 2023-01-29
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/override/final
- CPP/virtual/pure
---
**[[C++|HOME [C++]]]**

---
# Polymorphism: `Final`
- restrict how you override methods in derived classes
- restrict how you can derive from a base class

**e.g.**
```cpp
class Shape {
public:
    virtual void draw() = 0; // pure virtual function
};

class Rectangle : public Shape {
public:
    void draw() final;
};

class Square : public Rectangle {
public:
    // This line will give error because the draw function in the base class is marked as final
    void draw() override; 
};
```
```cpp
class Base final {};

// This line will give error because the Base class is marked as final
class Derived : public Base {};
```

**More examples:**
- [[C++polymorphismfinalsample0|Using `final` among inheritance]]

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/final