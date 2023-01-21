---
title: C++setters&getters
creation-date: 2023-01-19
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor/get
- CPP/Class/Constructor/set
---
**[[C++|HOME [C++]]]**

---
# Setters & Getters
method to read/modify member variables of a class
> same as [[C++classconstructorsdefaulted|default]], they must be set **public**

**e.g.**
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
    cylinder() = default; // empty constructor

    cylinder(double radius_param, double height_param) {
        base_radius = radius_param;
        height = height_param;
    }

    double volume() { return PI * pow(base_radius, 2) * height; }

    // Getter
    double get_base_radius() { return base_radius; }
    double get_height() { return height; }

    // Setter
    void set_base_radius(double radius_param) { base_radius = radius_param; }
    void set_height(double height_param) { height = height_param; }
};

int main(int argc, char **argv) {
    cylinder func1(10, 10); // class object

    std::cout << "volume: " << func1.volume() << std::endl;

    // Modify private member using getter/setter
    func1.set_base_radius(100);
    func1.set_height(20);

    std::cout << "volume: " << func1.volume() << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- 