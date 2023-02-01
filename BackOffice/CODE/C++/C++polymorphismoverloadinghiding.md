---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/override
---
**[[C++|HOME [C++]]]**

---
## Overloading, overriding, & hiding
>[!column|no-t flex]
>>[!INFO|no-i clean ttl-c collapse] OVERLOADING
>> the ability of a class or function to have multiple definitions with different parameters
>
>>[!INFO|no-i clean ttl-c collapse] OVERRIDING
>> the ability of a derived class to provide a different implementation of a method that is already provided by its base class
>
>>[!INFO|no-i clean ttl-c collapse] HIDING
>> when a derived class declares a new member with the same name as an existing member in the base class

>[!grid]
> ![[Pasted image 20230129112327.png]]
> ![[Pasted image 20230129112448.png]]

![[Pasted image 20230129112538.png]]
![[Pasted image 20230129112644.png]]

**e.g.**
```cpp
#include <iostream>
#include <string_view>
#include <string>

class Shape {
public:
    Shape() = default;
    Shape(std::string_view description)
        : m_description(description) {}
    ~Shape() {}

    virtual void draw() const {
        std::cout << "Shape::draw() called. Drawing " << m_description << std::endl;
    }

    virtual void draw(int colorDepth) const {
        std::cout << "Shape::draw() w/ colorDepth: " << colorDepth << std::endl;
    }

    /*
    virtual void draw(int colorDepth, std::string_view color) const {
        std::cout << "Circle::draw() with colorDepth & color called: " << colorDepth
                  << " " << color << std::endl;
    }
    */

protected:
    std::string m_description{""};
};

class Oval : public Shape {
public:
    Oval() = default;
    Oval(double x_radius, double y_radius,
         std::string_view description)
        : Shape(description), m_x_radius(x_radius), m_y_radius(y_radius) {}

    ~Oval() {}

    virtual void draw() const override {
        std::cout << "Oval::draw() called. Drawing " << m_description << " with m_x_radius : " << m_x_radius << " and m_y_radius : " << m_y_radius
                  << std::endl;
    }

    virtual void draw(int colorDepth, std::string_view color) const override {
        std::cout << "Oval::draw() with colorDepth & color called: " << colorDepth
                  << " " << color << std::endl;
    }

public:
    double get_x_rad() const { return m_x_radius; }
    double get_y_rad() const { return m_y_radius; }

private:
    double m_x_radius{0.0};
    double m_y_radius{0.0};
};

class Circle : public Oval {
public:
    Circle() = default;
    Circle(double radius, std::string_view description)
        : Oval(radius, radius, description) {}

    ~Circle() {}

    virtual void draw() const override {
        std::cout << "Circle::draw() called. Drawing " << m_description << " with radius : " << get_x_rad() << std::endl;
    }
};

int main() {
    Shape *shape_ptr = new Circle(10, "Circle1");

    // Shape class does not have a draw function that takes two arguments
    // Override the draw function in the Shape class
    shape_ptr->draw(12, "red");

    return 0;
}
```