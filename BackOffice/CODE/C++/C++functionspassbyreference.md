---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
- CPP/References
---
**[[C++|HOME [C++]]]**

---
## [[C++functions|Function]]: Pass by Reference
```cpp
#include <iostream>
void say_age(int &);

int main() {
    int age{23};

    std::cout << "age(before): " << age << std::endl;
    say_age(age);
    std::cout << "\nage(after): " << age << std::endl;

    return 0;
}

void say_age(int &a) {
    ++a;
    std::cout << "\nYou are " << a << std::endl;
}
```