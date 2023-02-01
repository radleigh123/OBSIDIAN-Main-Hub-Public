---
title: C++inheritance
creation-date: 2023-01-21
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Class/Constructor
- CPP/Class/Destructor
- CPP/Preprocessor/define
- CPP/Preprocessor/conditional/endif
- CPP/Preprocessor/conditional/ifndef
---
**[[C++|HOME [C++]]]**

---
# Inheritance
is a feature of the language that a derived class can inherit all or some of the data members and member functions of a base class, and can also add new members or override inherited members.
![[C++inheritanceillu1.png|cover wm-tl center]]
>[!NOTE|alt-co]+ NOTE
>- With **public inheritance**, derived classes can access and use public members of the base class, but the derived class can't directly access private members
>- The same also applies to friends of the derived class. They have access to private members of derived, but don't have access to the base class

```cpp
#include <iostream>

class Vehicle {
protected:
    int wheels;
    float engineSize;

public:
    Vehicle(int w, float e) {
        wheels = w;
        engineSize = e;
    }
    void printSpecs() {
        std::cout << "Wheels: " << wheels << std::endl;
        std::cout << "Engine size: " << engineSize << std::endl;
    }
};

class Car : public Vehicle {
private:
    int doors;
    float trunkSize;

public:
    Car(int w, float e, int d, float t) : Vehicle(w, e) {
        doors = d;
        trunkSize = t;
    }
    void printSpecs() {
        Vehicle::printSpecs();
        std::cout << "Doors: " << doors << std::endl;
        std::cout << "Trunk size: " << trunkSize << std::endl;
    }
};

int main() {
    Car myCar(4, 2.5, 4, 15);
    myCar.printSpecs();
    return 0;
}
```

**Example:**
- [[C++inheritancesample1|inheritance across multiple files]]

<br>

# 
---
- https://en.cppreference.com/book/intro/inheritance