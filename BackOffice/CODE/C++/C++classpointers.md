---
aliases:
tags:
- CPP/Lecture
- CPP/Class
- CPP/Pointers
- CPP/typedef
- CPP/Expressions/delete
---
**[[C++|HOME [C++]]]**

---
## Class: Managing class objects through pointers
**e.g.**
- [[C++classpointerssample0|Pointer to member function]]
- [[C++classpointerssample1|Pointer to member object]]
- [[C++classpointerssample2|Declaring pointers to a method]]
- [[C++classpointerssample3|Declaring pointer using `typedef`]]

<br>

**main.cpp**
```cpp
#include <iostream>
#include "cylinder.h"
#include "constants.h"

int main(int argc, char **argv) {
    cylinder func1(10, 10);
    cylinder *ptr_func1{&func1}; // Stack object through pointers
    
    // longer alternative: (*ptr_func).volume()
    std::cout << "volume: " << ptr_func1->volume() << std::endl;

    // cylinder heap through `new`
    cylinder *ptr_func2{new cylinder(100, 2)}; // heap object
    std::cout << "volume: " << ptr_func2->volume() << std::endl;
    std::cout << "base_radius(cylinder2): " << ptr_func2->get_base_radius() << std::endl;

    delete ptr_func2; // always good practice to release
    return 0;
}
```

>[!column|no-t]
>>[!INFO|no-i clean collapse] **cylinder.cpp**
>> ```cpp
>> #include "cylinder.h"
>> 
>> cylinder::cylinder(double radius_param, double height_param) {
>> 	base_radius = radius_param;
>> 	height = height_param;
>> }
>> 
>> double cylinder::volume() { return PI * base_radius * base_radius * height; }
>> 
>> // Getter
>> double cylinder::get_base_radius() { return base_radius; }
>> double cylinder::get_height() { return height; }
>> 
>> // Setter
>> void cylinder::set_base_radius(double radius_param) { base_radius = radius_param; }
>> void cylinder::set_height(double height_param) { height = height_param; }
>> ```
>
>>[!INFO|no-i clean collapse] **constants.h**
>> ```cpp
>> // if constants.h is not define, then define
>> // else, ignore define
>> #ifndef CONSTANTS_H
>> #define CONSTANTS_H
>> 
>> const double PI{3.1415926535897932384626433832795};
>> 
>> #endif
>> ```
>> &nbsp
>> &nbsp
>> &nbsp
>>
>> **cylinder.h**
>> ```cpp
>> // if cylinder.h is not define, then define
>> // else, ignore define
>> #ifndef CYLINDER_H
>> #define CYLINDER_H
>> #include "constants.h"
>> 
>> class cylinder {
>> private:
>> 	// Member variables
>> 	double base_radius{1};
>> 	double height{1};
>> 	
>> public:
>> 	cylinder() = default;                               // empty constructor
>> 	cylinder(double radius_param, double height_param); // prototype
>> 	double volume();                                    // prototype
>> 	
>> 	double get_base_radius();
>> 	double get_height();
>> 	
>> 	void set_base_radius(double radius_param);
>> 	void set_height(double height_param);
>> };
>> 
>> #endif
>> ```