---
aliases:
tags:
- CPP/Polymorphism
- CPP/Library/vector/vector
---
**[[C++polymorphism|BACK]]**

---
## Basic sample using vector
```cpp
#include <iostream>
#include <vector>

class Shape {
public:
    virtual void draw() { std::cout << "Drawing Shape...\n"; }
};

class Circle : public Shape {
public:
    void draw() override { std::cout << "Drawing Circle...\n"; }
};

class Square : public Shape {
public:
    void draw() override { std::cout << "Drawing Square...\n"; }
};

int main() {
    // Using polymorphism with a vector of Shape pointers
    std::vector<Shape*> shapes;
    shapes.push_back(new Circle());
    shapes.push_back(new Square());
    shapes.push_back(new Circle());

    for (auto shape : shapes) {
        shape->draw();
    }

    // Clean up dynamically created objects
    for (auto shape : shapes) {
        delete shape;
    }

    return 0;
}
```