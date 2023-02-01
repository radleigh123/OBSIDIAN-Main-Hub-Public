---
aliases:
tags:
- CPP/Polymorphism
---
**[[C++polymorphism|BACK]]**

---
## Difference between static and dynamic binding
> Think of a **Shape** class as a blueprint for creating shapes. This class has a **draw** function which is used to draw a shape. Now, we have two shapes we want to draw - a **Circle** and a **Square**. These two shapes inherit from the **Shape** class and have their own unique **draw** function which is used to draw the specific shape. Now, when you want to draw one of these shapes, you have two options:
> 1. You can tell the computer exactly which shape you want to draw. This is called "Static Binding". It happens at compile-time, meaning before the program runs. The computer knows exactly which **draw** function to use because you have told it exactly which shape you want to draw.
> 2. You can tell the computer that you want to draw a **Shape**, but you don't specify which one until the program is running. This is called "Dynamic Binding". It happens at runtime, meaning while the program is running. The computer determines which **draw** function to use based on the shape that it needs to draw at that moment.

<br>

```cpp
#include <iostream>

class Shape {
public:
    virtual void draw() {
        std::cout << "Shape::draw" << std::endl;
    }
};

class Circle : public Shape {
public:
    void draw() {
        std::cout << "Circle::draw" << std::endl;
    }
};

class Square : public Shape {
public:
    void draw() {
        std::cout << "Square::draw" << std::endl;
    }
};

int main() {
    // Static binding (early binding)
    Shape shape;
    shape.draw(); // Output: Shape::draw

    // Dynamic binding (late binding)
    Shape *shapePointer;
    Circle circle;
    shapePointer = &circle;
    shapePointer->draw(); // Output: Circle::draw

    Square square;
    shapePointer = &square;
    shapePointer->draw(); // Output: Square::draw

    return 0;
}
```