---
title: C++polymorphismvirtualdestructors
creation-date: 2023-01-30
aliases:
tags:
- CPP/Lecture
- CPP/virtual/destructors
- CPP/Class/Destructor
- CPP/Polymorphism
---
**[[C++|HOME [C++]]]**

---
# Virtual destructors
deleting a derived class object using a pointer of base class type that has a non-virtual destructor results in undefined behavior. To correct this situation, the base class should be defined with a virtual destructor.
**e.g.**
```cpp
#include <iostream>
#include <string>
#include <string_view>

class Base {
public:
    Base() = default;
    Base(std::string_view description)
        : m_description(description) {}

    virtual ~Base() { std::cout << "Base destructor called" << std::endl; }

    virtual void breathe() const {
        std::cout << "Base::breathe called for : " << m_description << std::endl;
    }

protected:
    std::string m_description;
};

class Derived1 : public Base {
public:
    Derived1() = default;
    Derived1(std::string_view fur_style, std::string_view description)
        : Base(description), m_fur_style(fur_style) {}

    virtual ~Derived1() { std::cout << "Derived1 destructor called" << std::endl; }

    virtual void run() const {
        std::cout << "Derived1 " << m_description << " is running" << std::endl;
    }
    std::string m_fur_style;
};

class Derived2 : public Derived1 {
public:
    Derived2() = default;
    Derived2(std::string_view fur_style, std::string_view description)
        : Derived1(fur_style, description) {}

    virtual ~Derived2() { std::cout << "Derived2 destructor called" << std::endl; }

    virtual void bark() const {
        std::cout << "Derived2::bark called : Woof!" << std::endl;
    }
};

int main(int argc, char **argv) {
    Base *ptr{new Derived2};
    // If no virtual added, it will only call Base destructor

    delete ptr;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://www.geeksforgeeks.org/virtual-destructor/