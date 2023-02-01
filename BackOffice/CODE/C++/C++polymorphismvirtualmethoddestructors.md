---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Class/Constructor
- CPP/Class/Destructor
- CPP/virtual
- CPP/Polymorphism
---
**[[C++|HOME [C++]]]**

---
## Don't call virtual polymorphic functions from [[C++classconstructors|constructors]] & [[C++classdestructors|destructors]]
calling a virtual function from a constructor or destructor can result in undefined behavior because the object's complete class type may not yet have been fully constructed or already partially destroyed.
- Calling a virtual function from a constructor/destructor won't give you polymorphic results
- The call will never go to a more derived class than the currently executing constructor/destructor
- In other words you will get static binding results

**e.g.**
```cpp
#include <iostream>

class Base {
public:
    Base() {
        std::cout << "Base constructor called" << std::endl;
        // this->setup(); // UNDEFINED! Static binding kicks here
    }
    virtual ~Base() {
        // this->clean_up(); // UNDEFINED!
        std::cout << "Base destructor called" << std::endl;
    }

    virtual void setup() {
        std::cout << "Base::setup() called" << std::endl;
        m_value = 10;
    }
    virtual void clean_up() {
        std::cout << "Base::clean_up() called" << std::endl;
    }
    int get_value() { return m_value; }

protected:
    int m_value;
};

class Derived : public Base {
public:
    Derived() : Base() { std::cout << "Derived constructor called" << std::endl; }
    virtual ~Derived() { std::cout << "Derived destructor called" << std::endl; }

    virtual void setup() override {
        std::cout << "Derived::setup() called" << std::endl;
        m_value = 100;
    }
    virtual void clean_up() override {
        std::cout << "Derived::clean_up() called" << std::endl;
    }
};

int main() {
    Base *p_base = new Derived;

    p_base->setup(); // call virtual function

    auto value = p_base->get_value();
    std::cout << value << std::endl;

    p_base->clean_up();

    delete p_base;

    return 0;
}
```