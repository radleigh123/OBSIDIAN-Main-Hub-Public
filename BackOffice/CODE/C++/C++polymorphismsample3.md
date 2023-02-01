---
aliases:
tags:
- CPP/Polymorphism
---
**[[C++polymorphism|BACK]]**

---
## Static binding with base class pointer/reference
>[!WARNING|ttl-c alt-co] Use with caution
> ```cpp
> void draw_circle(const Circle &circle) { circle.draw(); } // to call Circle::draw()
> void draw_oval(const Oval &oval) { oval.draw(); } // to call Oval::draw()
> ```

**main.cpp**
```cpp
#include <iostream>
#include "base.h"
#include "oval.h"
#include "circle.h"

int main() {
    Base b1("Shape1");
    Oval o1(2.5, 3.45, "Oval");
    Circle c1(3.45, "Circle");

    // Base pointers
    Base *base_ptr = &b1;
    base_ptr->draw();

    base_ptr = &o1;
    base_ptr->draw();

    base_ptr = &c1;
    base_ptr->draw();

    return 0;
}
```
>[!column|no-t]
>>[!INFO|clean no-i] base.h
>> ```cpp
>> #ifndef BASE_H
>> #define BASE_H
>> 
>> #include <string>
>> #include <string_view>
>> #include <iostream>
>> 
>> class Base {
>> public:
>>     Base() = default;
>>     Base(std::string_view description);
>>     ~Base();
>> 
>>     void draw() const {
>>         std::cout << "Base::draw() called... Drawing " << m_description << std::endl;
>>     }
>> 
>> protected:
>>     std::string m_description{""};
>> };
>> 
>> #endif // BASE_H
>> ```
>
>>[!INFO|clean no-i] base.cpp
>> ```cpp
>> #include "base.h"
>> 
>> Base::Base(std::string_view description) : m_description(description) {}
>> Base::~Base() {}
>> ```

>[!column|no-t]
>>[!INFO|clean no-i] oval.h
>> ```cpp
>> #ifndef OVAL_H
>> #define OVAL_H
>> 
>> #include "base.h"
>> 
>> class Oval : public Base {
>> public:
>>     Oval() = default;
>>     Oval(double x_radius,
>>          double y_radius,
>>          std::string_view description);
>>     ~Oval();
>> 
>>     void draw() const {
>>         std::cout << "\nOval::draw() called... Drawing " << m_description
>>                   << " with m_x_radius: " << m_x_radius
>>                   << " and m_y_radius: " << m_y_radius << std::endl;
>>     }
>> 
>> protected:
>>     double get_x_radius() const { return m_x_radius; }
>>     double get_y_radius() const { return m_y_radius; }
>> 
>> private:
>>     double m_x_radius{};
>>     double m_y_radius{};
>> };
>> 
>> #endif // OVAL_H
>> ```
>
>>[!INFO|clean no-i] oval.cpp
>> ```cpp
>> #include "oval.h"
>> 
>> Oval::Oval(double x_radius,
>>            double y_radius,
>>            std::string_view description) : Base(description), m_x_radius(x_radius), m_y_radius(y_radius) {}
>> 
>> Oval::~Oval() {}
>> ```

>[!column|no-t]
>>[!INFO|clean no-i] circle.h
>> ```cpp
>> #ifndef CIRCLE_H
>> #define CIRCLE_H
>> 
>> #include "oval.h"
>> 
>> class Circle : public Oval {
>> public:
>>     Circle() = default;
>>     Circle(double radius, std::string_view description);
>>     ~Circle();
>> 
>>     void draw() const {
>>         std::cout << "\nCircle::draw() called... Drawing " << m_description
>>                   << " with radius: " << get_x_radius() << std::endl;
>>     }
>> };
>> 
>> #endif // CIRCLE_H
>> ```
>
>>[!INFO|clean no-i] circle.cpp
>> ```cpp
>> #include "circle.h"
>> 
>> Circle::Circle(double radius, std::string_view description) : Oval(radius, radius, description) {}
>> Circle::~Circle() {}
>> ```