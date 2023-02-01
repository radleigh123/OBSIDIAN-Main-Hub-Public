---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/Class/Inheritance
- CPP/virtual/pure
---
**[[C++|HOME [C++]]]**

---
## Abstract classes as **interfaces**
>[!INFO|alt-co clean no-t]
>- an abstract class with only [[C++polymorphismpurevirtualfunctions|pure virtual functions]] and no member variable can be used to model what is called an interface in Object Oriented Programming
>- An interface is specification of something that will be fully implemented in a derived classes, but the specification itself resides in the abstract class

**Simple sample**
```cpp
#include <iostream>
#include <vector>

// Declare the abstract class Vehicle as an interface
class Vehicle {
public:
    // Declare a pure virtual function startEngine()
    virtual void startEngine() = 0;
};

// Derive concrete class Car from the abstract class Vehicle
class Car : public Vehicle {
public:
    // Override the startEngine() function to provide a concrete implementation
    void startEngine() override {
        std::cout << "The car's engine has started." << std::endl;
    }
};

// Derive concrete class Bike from the abstract class Vehicle
class Bike : public Vehicle {
public:
    // Override the startEngine() function to provide a concrete implementation
    void startEngine() override {
        std::cout << "The bike's engine has started." << std::endl;
    }
};

int main() {
    // Create a vector of pointers to Vehicle objects
    std::vector<Vehicle *> vehicles;
    vehicles.push_back(new Car());
    vehicles.push_back(new Bike());

    // Call the startEngine() function for each vehicle
    for (Vehicle *vehicle : vehicles) { vehicle->startEngine(); }
    return 0;
}
```

[[C++polymorphismabstractinterfacessample1|Complex sample]]