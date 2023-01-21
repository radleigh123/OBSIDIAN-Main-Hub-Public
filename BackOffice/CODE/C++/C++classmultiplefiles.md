---
aliases:
tags:
- CPP/Lecture
- CPP/Class
- CPP/Preprocessor/conditional/ifndef
- CPP/Preprocessor/define
- CPP/Preprocessor/conditional/endif
---
**[[C++|HOME [C++]]]**

---
## Class: Across multiple files
>[!INFO|alt-co no-i ttl-c]+ calling member function using scope resolution operator `::`
> ```cpp
> T class_name::memberfunction_name() {
> 	// body
> }
> ```
> 
> ```cpp
> // calling constructors
> class_name::class_name() {
> 	// body
> }
> ```

**e.g.**
>[!column|no-t]
>>[!INFO|no-i clean collapse] main.cpp
>> ```cpp
>> #include <iostream>
>> #include "cylinder.h"
>> 
>> int main(int argc, char **argv)
>> {
>> 	cylinder func1(10, 10);
>> 	
>> 	std::cout << func1.volume();
>> 	return 0;
>> }
>> ```
>> &nbsp
>> 
>> **cylinder.cpp**
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