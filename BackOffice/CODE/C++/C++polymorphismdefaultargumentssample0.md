---
aliases:
tags:
- CPP/Polymorphism
- CPP/Functions/default
- CPP/virtual
---
**[[C++polymorphismdefaultarguments|BACK]]**

---
## virtual function with default arguments
```cpp
#include <iostream>

class Base {
public:
    Base() {}
    ~Base() {}

    virtual double add(double a = 5, double b = 5) const {
        std::cout << "Base::add() called...";
        return (a + b + 1);
    }
};

class Derived : public Base {
public:
    Derived() {}
    ~Derived() {}

    virtual double add(double a = 10, double b = 10) const override {
        std::cout << "Derived::add() called... ";
        return (a + b + 2);
    }
};

int main(int argc, char **argv) {
    // Base ptr: uses polymorphism
    Base *base_ptr1 = new Derived;
    double result = base_ptr1->add();
    std::cout << "Result (base_ptr): " << result << std::endl;

    // Base ref: also uses polymorphism
    Derived derived1;
    Base &base_ref1 = derived1;
    result = base_ref1.add();
    std::cout << "Result (base_ref): " << result << std::endl;

    std::cout << "--------------------------" << std::endl;

    // Raw objects
    Base base3;
    result = base3.add();
    std::cout << "Result (base3): " << result << std::endl;

    std::cout << "--------------------------" << std::endl;

    // Direct objects: uses static binding
    Derived derived2;
    result = derived2.add();
    std::cout << "Result (direct object): " << result << std::endl;

    std::cout << "--------------------------" << std::endl;

    // raw objects - slicing: uses static binding
    Base base1 = derived2;
    result = base1.add();
    std::cout << "Result (raw objects assignment): " << result << std::endl;

    return 0;
}
```