---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/override/final
---
**[[C++|HOME [C++]]]**

---
## Override C++11
a keyword that helps to ensure that the function in the derived class is properly overriding the function in the base class, and can help to catch errors such as accidental name clashes or mismatched parameters.
**e.g.**
```cpp
class Base {
public:
    virtual void draw() const = 0;
};

class Derived : public Base {
public:
    // ensures this function is intended to override the
    // function in parent class
    virtual void draw() const override {
        std::cout << "Derived::draw() called..." << std::endl;
    }
};
```

>[!FAQ|alt-co]+ Things you should know
>- **[[C++polymorphismfinal|final]]** - keyword can be used to indicate that a virtual function cannot be overridden in a derived class.
>- <mark class="hltr-lightred">Using override in constructor or destructor is illegal</mark>

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/override