---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
---
**[[C++|HOME [C++]]]**

---
## Size of polymorphic objects & slicing
**e.g.**
```cpp
#include <iostream>

class Base { int x; };
class Derived : public Base { int y; };

int main() {
    Derived d;
    std::cout << "Size of Derived object: " << sizeof(d) << std::endl;

    Base *b = &d;
    std::cout << "Size of Base pointer pointing to Derived object: " << sizeof(b) << std::endl;
    // The size of a polymorphic object is determined by the size of the base class, not the size of the derived class.

    return 0;
}
```
<br>

>[!MISSING|alt-co ttl-c] Slicing
>> To avoid slicing, one should use pointers or references to the base class instead of copying the object.
>
> is a phenomenon that occurs when a derived class object is assigned to a base class object. When this happens, the compiler only copies the base class data members, and not the derived class data members. This results in loss of information, and is known as slicing.
> ```cpp
> Base b1("sample");
> Derived d1(2.5, 3.66, "sample1");
> 
> Base b2 = d1;
> ```