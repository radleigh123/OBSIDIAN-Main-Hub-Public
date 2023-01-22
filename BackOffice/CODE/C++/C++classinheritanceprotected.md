---
title: C++classprotected
creation-date: 2023-01-21
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Class/BaseClassAccessSpecifier/protected
- CPP/Preprocessor/define
- CPP/Preprocessor/conditional/endif
- CPP/Preprocessor/conditional/ifndef
---
**[[C++|HOME [C++]]]**

---
# `protected` members
access level is used for members (data members and member functions) of a class. It can only be accessed from within the class itself and from its derived classes.
```cpp
#include <iostream>

class Shape {
protected:
    int sides; // protected data member
public:
    Shape(int s) : sides(s) {} // constructor
    int getSides() {return sides;} // public member function
};

class Triangle : public Shape {
public:
    Triangle() : Shape(3) {} // constructor that calls the base class constructor
    void printInfo() {
        std::cout << "A triangle has " << sides << " sides." << std::endl;
        // sides is protected, so it can be accessed by this derived class
    }
};

int main() {
    Triangle t;
    t.printInfo();
    // std::cout << t.sides; // This will generate a compile error, because sides is 
    // protected and cannot be accessed directly from outside the class or the derived class.
}
```

**Example:**
- [[C++classprotectedsample1|protected w/ multiple files]]

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/access