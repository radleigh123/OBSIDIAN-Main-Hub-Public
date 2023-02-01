---
aliases:
tags:
- CPP/Polymorphism
- CPP/Class/Inheritance
- CPP/Conversion/dynamic_cast
---
**[[C++dynamiccast|BACK]]**

---
## Simple example 0
```cpp
#include <iostream>

class Shape {
public:
  virtual void draw() { std::cout << "Drawing Shape\n"; }
};

class Circle : public Shape {
public:
  virtual void draw() { std::cout << "Drawing Circle\n"; }
};

class Square : public Shape {
public:
  virtual void draw() { std::cout << "Drawing Square\n"; }
};

int main() {
  Shape *shape = new Circle;  // shape points to a Circle object

  // Use dynamic_cast to safely cast shape to a Circle pointer
  Circle *circle = dynamic_cast<Circle*>(shape);
  if (circle) {
    // The cast was successful, call draw() on the Circle object
    circle->draw();
  } else {
    // The cast failed, shape does not point to a Circle object
    std::cout << "Can't cast Shape to Circle\n";
  }

  return 0;
}
```