---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Inheritance and Polymorphism w/ Static members
**e.g.**
```cpp
#include <iostream>
#include <string>

class Shape {
public:
    static int m_count;
    Shape(std::string_view description)
        : m_description(description) { ++m_count; }

    Shape()
        : Shape("NoDescription") {}
    virtual ~Shape() { --m_count; }

    virtual int get_count() const { return m_count; }

protected:
    std::string m_description;
};

class Ellipse : public Shape {
public:
    static int m_count;

    Ellipse(double x_radius, double y_radius,
            std::string_view description)
        : Shape(description), m_x_radius(x_radius),
          m_y_radius(y_radius) { ++m_count; }

    Ellipse()
        : Ellipse(0.0, 0.0, "NoDescription") {}

    virtual ~Ellipse() { --m_count; }

    virtual int get_count() const override { return m_count; }

private:
    double m_x_radius;
    double m_y_radius;
};

int Shape::m_count{0}; // should initialize static variable with a value outside the class or function
int Ellipse::m_count{0};

int main() {
    // Shape
    Shape shape1("shape1");
    std::cout << "shape count: " << Shape::m_count << std::endl;

    Shape shape2("shape2");
    std::cout << "shape count: " << Shape::m_count << std::endl;

    Shape shape3;
    std::cout << "shape count: " << Shape::m_count << std::endl;

    std::cout << "---------------------------------" << std::endl;

    // Ellipse
    Ellipse ellipse(10, 12, "ellipse");
    std::cout << "shape count: " << Shape::m_count << std::endl;
    std::cout << "ellipse count: " << Ellipse::m_count << std::endl;

    std::cout << "---------------------------------" << std::endl;

    // Shape polymorphism
    Shape *shape4[]{&shape1, &ellipse};
    for (const auto &i : shape4) std::cout << "count: " << i->get_count() << std::endl;

    return 0;
}
```