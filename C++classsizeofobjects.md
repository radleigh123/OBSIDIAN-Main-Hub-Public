---
aliases:
tags:
- CPP/Lecture
- CPP/Class
---
**[[C++|HOME [C++]]]**

---
## Size of class objects
```cpp
#include <iostream>

class myClass {
public:
    myClass() = default;

private:
    size_t m_var1, m_var2; // 16
    int *ptrAge;           // 8

    // no matter how you would change the text, this one goes to pointers
    std::string name{"Hello World"}; // 6
};

int main(int argc, char **argv) {
    myClass func1;

    std::cout << "size(size_t): " << sizeof(size_t) << std::endl; // 8
    std::cout << "sizeof(int *): " << sizeof(int *) << std::endl; // 8
    std::cout << "sizeof(std::string): " << sizeof(std::string) << std::endl;

    std::cout << "\nsize(myClass): " << sizeof(myClass) << std::endl; // 24

    return 0;
}
```

>[!NOTE|alt-co bg-purple]+ Boundary alignment