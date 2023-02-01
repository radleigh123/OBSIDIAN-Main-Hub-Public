---
aliases:
tags:
- CPP/Class
- CPP/Pointers/this
- CPP/Class/Constructor
- CPP/Library/string_view/string_view
---
**[[C++classthethispointer|BACK]]**

---
>[!recite|clean no-i] Printing out object addresses
```cpp
#include <iostream>
#include <string_view>

class myClass {
public:
    myClass() = default;
    myClass(std::string_view name_param, std::string_view sex_param, int age_param);
    ~myClass(); // defining destructor

private:
    std::string name, sex;
    int *ptr_age{nullptr};
};

myClass::myClass(std::string_view name_param, std::string_view sex_param, int age_param) {
    name = name_param;
    sex = sex_param;
    ptr_age = new int;
    *ptr_age = age_param;

    std::cout << "myClass constructor called value: " << name << " at " << this << std::endl;
}

myClass::~myClass() {
    delete ptr_age;
    std::cout << "myClass destructor called value: " << name << " at " << this << std::endl;
}

int main(int argc, char **argv) {
    myClass func1("Fluffy", "Gay", 22); // constructor called

    std::cout << "Done" << std::endl; // destructor called
    return 0;
}
```