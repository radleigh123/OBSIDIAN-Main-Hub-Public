---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor/default
---
**[[C++|HOME [C++]]]**

---
## Default constructors
if there are any constructors in a class and no default constructor was initialized, compiler will give error
> **default constructors** have to be public, to be accessible

**e.g.**
```cpp
#include <iostream>
#include <cmath>
const double PI{3.1415926535897932384626433832795};

class cylinder {
private:
    double base_radius{1};
    double height{1};

public:
    cylinder() = default; // empty constructor

    cylinder(double radius_param, double height_param) {
        base_radius = radius_param;
        height = height_param;
    }

    double volume() { return PI * pow(base_radius, 2) * height; }
};

int main(int argc, char **argv) {
    cylinder func1; // class object

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/default_constructor#Eligible_default_constructor