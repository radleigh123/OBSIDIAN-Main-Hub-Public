---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## Returning from functions
**Returning from functions (Default is by value)**
In modern compilers, return by value is commonly optimized out by the compiler when possible and the function is modified behind your back to return by reference, avoiding unnecessary copies

```cpp
#include <iostream>
int sum(int, int);

int main(int argc, char **argv) {
    int a{45}, b{16}, result = sum(a, b);

    std::cout << "Out(&result(int)): " << &result << std::endl;
    std::cout << "Sum: " << result << std::endl;

    return 0;
}

int sum(int num1, int num2) {
    int result1 = num1 + num2;
    std::cout << "In(&result1(int)): " << &result1 << std::endl;

    return result1;
}
```

**Compiler's optimization to return by [[C++references|reference]]** // still not return by reference
```cpp
#include <iostream>
std::string add_strings(std::string, std::string);

int main(int argc, char **argv) {
    std::string str{add_strings(std::string("Hello"), std::string(" World!"))};

    std::cout << "Out (&str(std::string)): " << &str << std::endl;
    std::cout << "str: " << str << std::endl;

    return 0;
}

std::string add_strings(std::string a, std::string b) {
    std::string result{a + b};
    std::cout << "In (&result(std::string)): " << &result << std::endl;

    return result;
}
```