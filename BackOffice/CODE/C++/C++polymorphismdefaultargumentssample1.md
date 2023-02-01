---
aliases:
tags:
- CPP/Polymorphism
- CPP/Functions/default
- CPP/Class/Inheritance
---
**[[C++polymorphismdefaultarguments|BACK]]**

---
## Sample 1
```cpp
#include <iostream>

class Base {
public:
    virtual void draw(int a = 5, int b = 5) {
        std::cout << "Base::draw() called... " << a << ", " << b << std::endl;
    }
};

class Derived : public Base {
public:
    void draw(int a = 10, int b = 10) override {
        std::cout << "Derived::draw() called... " << a << ", " << b + 2 << std::endl;
    }
};

int main(int argc, char **argv) {
    Base *base_ptr = new Derived();
    base_ptr->draw(); // default values will not be overridden by Derived class
    delete base_ptr;

    return 0;
}
```