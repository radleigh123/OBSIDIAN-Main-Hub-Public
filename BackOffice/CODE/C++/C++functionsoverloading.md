---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
- CPP/Strings
- CPP/Library/string/string
- CPP/Library/string_view/string_view
---
**[[C++|HOME [C++]]]**

---
## Function Overloading
> **Not recommended**

```cpp
// Compiler function overload will work if order, number, & type is different
int foo(int a, int b);
int foo(double a, int b);
```
- Order
- Number
- Types

**e.g.**
```cpp
#include <iostream>
int max(int a, int b);
double max(double a, double b);
std::string_view max(std::string_view a, std::string_view b);

int main(int argc, char **argv) {
    int num1{41}, num2{29};
    double dob1{47.2}, dob2{55.01};
    std::string_view str1{"abcd"}, str2{" abcc"};

    std::cout << "max (" << num1 << ", " << num2 << "): " << max(num1, num2) << std::endl;
    std::cout << "max (" << 5 << ", " << 7 << "): " << max(5, 7) << std::endl;

    std::cout << "\nmax (" << dob1 << ", " << dob2 << "): " << max(dob1, dob2) << std::endl;

    std::cout << "\nmax (" << str1 << ", " << str2 << "): " << max(str1, str2) << std::endl;
    std::cout << "max(abcd, abce): " << max("abcd", "abce") << std::endl;

    return 0;
}

/*
// Can't overload on the return type. Compiler error
double max(int a, int b) { return (a > b) ? a : b; }
*/

int max(int a, int b) { return (a > b) ? a : b; }
double max(double a, double b) { return (a > b) ? a : b; }
std::string_view max(std::string_view a, std::string_view b) { return (a > b) ? a : b; }
```