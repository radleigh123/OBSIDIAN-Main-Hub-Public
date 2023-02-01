---
aliases:
tags:
- CPP/Polymorphism
- CPP/virtual
---
**[[C++polymorphism|BACK]]**

---
## Basic sample
**main.cpp**
```cpp
#include <iostream>
#include "class.h"

int main() {
    Base *f1[3];
    f1[0] = new Base();
    f1[1] = new Derived2();
    f1[2] = new Derived3();

    for (size_t i = 0; i < 3; i++) { f1[i]->makeSound(); }

    return 0;
}
```
>[!column|no-t]
>>[!INFO|clean no-i] class.h
>> ```cpp
>> #ifndef CLASS_H
>> #define CLASS_H
>> 
>> class Base {
>> public:
>>     virtual void makeSound();
>> };
>> 
>> class Derived2 : public Base {
>> public:
>>     void makeSound() override;
>> };
>> 
>> class Derived3 : public Base {
>> public:
>>     void makeSound() override;
>> };
>> 
>> #endif
>> ```
>
>>[!INFO|clean no-i] class.cpp
>> ```cpp
>> #include <iostream>
>> #include "class.h"
>> 
>> void Base::makeSound() { std::cout << "Some sounds" << std::endl; }
>> void Derived2::makeSound() { std::cout << "Derived2..." << std::endl; }
>> void Derived3::makeSound() { std::cout << "Derived2..." << std::endl; }
>> ```