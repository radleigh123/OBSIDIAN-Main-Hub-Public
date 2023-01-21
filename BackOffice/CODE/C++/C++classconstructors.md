---
cssclass: bl-c
title: C++constructors
creation-date: 2023-01-19
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor
- CPP/Library/cmath/pow
---
**[[C++|HOME [C++]]]**

---
# Class: Constructors
a special kind of method that is called when an instance of a class is created
- no return type
- same name as the class
- can have parameters. Can also have an empty parameter list
- usually used to initialize member variables of a class

```cpp
#include <iostream>
#include <cmath>
const double PI{3.1415926535897932384626433832795};

class cylinder {
private:
    // Member variables
    double base_radius{1};
    double height{1};

public:
    // if no constructor, compiler creates empty constructor
    cylinder(){}

    // constructor w/out parameters
    cylinder() {
        base_radius = 2.0;
        height = 2.0;
    }

    // constructor w/ parameters
    cylinder(double radius_param, double height_param) {
        base_radius = radius_param;
        height = height_param;
    }

    double volume() { return PI * pow(base_radius, 2) * height; }
};

int main(int argc, char **argv) {
    cylinder func1(10, 4); // class object w/ parameters

    std::cout << "func1: " << func1.volume() << std::endl;
    return 0;
}
```

>[!NOTE] constructor initializer list
> ```cpp
> className(int x) : x(x) {}
> ```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/constructor