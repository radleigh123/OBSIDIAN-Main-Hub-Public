---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
---
**[[C++|HOME [C++]]]**

---
## [[C++functions|Function]]: Pass by value
```cpp
#include <iostream>
void say_age(int);

int main() {
    int age{31};

    std::cout << "Age(before): " << age << std::endl;
    say_age(age);
    std::cout << "\nAge(after): " << age << std::endl;

    return 0;
}

void say_age(int a) {
    a++;
    std::cout << "\nYou are " << a << " - say_age function" << std::endl;
}
```