---
title: C++struct
creation-date: 2023-01-20
aliases:
tags:
- CPP/Lecture
- CPP/Struct
---
**[[C++|HOME [C++]]]**

---
# Struct
is a type consisting of a sequence of members whose storage is allocated in an ordered sequence (as opposed to union, which is a type consisting of a sequence of members whose storage overlaps).
**e.g.**
```cpp
#include <iostream>

class myClass {
    // `m_name` commonly used, meaning member variable
    std::string m_name;
};

struct myStruct {
    std::string m_name;
};

int main(int argc, char **argv) {
    myClass func1;
    myStruct p1;

    func1.m_name = "Sins"; // Error! class member is private by default
    p1.m_name = "Johhny";

    std::cout << func1.m_name << std::endl;
    std::cout << p1.m_name << std::endl;
    return 0;
}
```

>[!NOTE|alt-co]+ `struct` is mostly useful if you want to set up classes that only have public member variables and member functions/methods are not necessary
> ```cpp
> #include <iostream>
> 
> struct Point {
> 	double x, y;
> };
> 
> void print(const Point &point) {
> 	std::cout << "Point [x: " << point.x << ", y: " << point.y << "]" << std::endl;
> }
> 
> int main(int argc, char **argv) {
> Point p1;
> 
> p1.x = 10;
> p1.y = 15.5;
> print(p1);
> 
> p1.x = 40.4;
> p1.y = 2.7;
> print(p1);
> 
> return 0;
> }
> ```


<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/c/language/struct