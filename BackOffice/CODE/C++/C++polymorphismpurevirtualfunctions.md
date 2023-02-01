---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Polymorphism
- CPP/virtual/pure
- CPP/typeid
- CPP/Pointers
- CPP/const
---
**[[C++|HOME [C++]]]**

---
## Pure virtual functions & abstract classes
**Pure virtual function**
- is a [[C++polymorphismdynamicbinding|virtual function]] that has no implementation in the base class and must be defined in derived classes.
- act as a placeholder for the derived classes to provide their own implementation and make the base class an abstract class, which cannot be instantiated on its own.

>[!NOTE|alt-co]-
>- If a class has at least one pure virtual function, it becomes an abstract class
>- You can't create objects of an abstract class, if you do that, you'll get a hard compiler error
>- Derived classes from an abstract class must explicitly override all the pure virtual functions from the abstract parent class, if they don't they themselves become abstract
>- Pure virtual functions don't have an implementation in the abstract class. They are meant to be implemented by deriving classes
>- You can't call the pure virtual functions from the constructor of the abstract class
>- The constructor of the abstract class is used by deriving class to build up the base part of the object

>[!EXAMPLE|alt-co]- For example:
> ```cpp
> #include <iostream>
> 
> class Shape {
> public:
>     virtual float area() = 0; // change this into `{}` and it will expect a return value
> };
> 
> class Rectangle : public Shape {
> private:
>     float width, height;
> 
> public:
>     Rectangle(float w, float h) : width(w), height(h) {}
>     float area() { return width * height; }
> };
> 
> class Circle : public Shape {
> private:
>     float radius;
> 
> public:
>     Circle(float r) : radius(r) {}
>     float area() { return 3.14159 * radius * radius; }
> };
> 
> int main() {
>     Shape *ptr_shape{new Rectangle(5, 10)};
>     std::cout << "Area of Rectangle: " << ptr_shape->area() << std::endl;
> 
>     ptr_shape = new Circle(2);
>     std::cout << "Area of Circle: " << ptr_shape->area() << std::endl;
> 
>     delete ptr_shape;
> 
>     return 0;
> }
> ```

**e.g.**
```cpp
#include <iostream>
#include <string>

class Shape {
protected:
    Shape() = default;
    Shape(std::string_view description) : m_description(description) {}

public:
    virtual ~Shape() = default; // If destructor is not public, you won't be
                                // able to delete base_ptrs.
    // Pure virtual functions
    virtual double perimeter() const = 0;
    virtual double surface() const = 0;

private:
    std::string m_description;
};

class Circle : public Shape {
public:
    Circle() = default;
    Circle(double radius, std::string_view description)
        : Shape(description), m_radius(radius) {}
    virtual ~Circle() = default;

    virtual double perimeter() const { return (2 * PI * m_radius); }
    virtual double surface() const { return PI * m_radius * m_radius; }

private:
    double m_radius{0.0};

    inline static double PI{3.14159265};
};

class Rectangle : public Shape {
public:
    Rectangle() = default;
    Rectangle(double width, double height, std::string_view description)
        : Shape(description), m_width(width), m_height(height) {}
    virtual ~Rectangle() = default;

public:
    virtual double perimeter() const override { return (2 * m_width + 2 * m_height); }
    virtual double surface() const override { return (m_width * m_height); }

private:
    double m_width{0.0};
    double m_height{0.0};
};

int main() {
    // Shape *shape_ptr{new Shape};
    const Shape *shape_rect1{new Rectangle(10, 10, "rect1")}; // e.g., shape_rect1->setWidth(20) ERROR! becuase `const`
    double surface{shape_rect1->surface()};
    std::cout << "Dynamic type of shape_rect1: " << typeid(*shape_rect1).name() << std::endl;
    std::cout << "The surface of shape_rect1: " << surface << std::endl;

    std::cout << "---------------------------------" << std::endl;

    const Shape *shape_circle1{new Circle(10, "circle1")};
    surface = shape_circle1->surface();
    std::cout << "Dynamic type of shape_circle1: " << typeid(*shape_circle1).name() << std::endl;
    std::cout << "The surface of the circle1: " << surface << std::endl;

    return 0;
}
```