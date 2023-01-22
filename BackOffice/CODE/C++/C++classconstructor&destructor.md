---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Destructor
- CPP/Class/Constructor
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## Constructor & Destructor call order
- [[C++classconstructors|constructors]] are called in the order of inheritance, starting with the most derived class and working backwards to the base class.
- [[C++classdestructors|destructors]] are called in the opposite order, starting with the base class and working forwards to the most derived class. This is known as the "constructor/destructor chain" or "object life cycle".

```cpp
#include <iostream>

class Base {
public:
    Base() {
        std::cout << "Base class constructor called" << std::endl;
    }
    ~Base() {
        std::cout << "Base class destructor called" << std::endl;
    }
};

class Derived : public Base {
public:
    Derived() {
        std::cout << "Derived class constructor called" << std::endl;
    }
    ~Derived() {
        std::cout << "Derived class destructor called" << std::endl;
    }
};

int main() {
    std::cout << "Creating object of Derived class" << std::endl;
    Derived d;
    std::cout << "Object of Derived class created" << std::endl;
    return 0;
}
```

**e.g.**
```cpp
#include <iostream>
#include <string_view>

class myClass {
public:
    myClass() = default;
    myClass(std::string_view name_param, std::string_view age_param, int grade_param);
    ~myClass();

private:
    std::string name, age;
    int *ptrgrade{nullptr};
};

myClass::myClass(std::string_view name_param, std::string_view age_param, int grade_param) {
    name = name_param;
    age = age_param;
    ptrgrade = new int; // memory allocated on heap
    *ptrgrade = grade_param;
    std::cout << "Constructor called value: " << name << std::endl;
}

myClass::~myClass() {
    delete ptrgrade;
    std::cout << "Destructor called value: " << name << std::endl;
}

int main(int argc, char **argv) {
    myClass p1("Person1", "Sex1", 1);
    myClass p2("Person2", "Sex2", 2);
    myClass p3("Person3", "Sex3", 3);
    myClass p4("Person4", "Sex4", 4);

    return 0;
}
```