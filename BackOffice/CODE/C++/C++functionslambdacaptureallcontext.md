---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
---
**[[C++|HOME [C++]]]**

---
## [[C++functionslambda|Lambda function]]: Capture all in context
**Capture by value**
```cpp
#include <iostream>

int main(int argc, char **argv) {
    int num1{42};
    
    // `=` syntax lets access outside this function
    auto func = [=](){
        std::cout << "Inner value: " << num1
                  << "\t" << &num1 << std::endl;
    };

    for (size_t i = 0; i < 3; i++) {
        std::cout << "\nOuter value: " << num1
                  << "\t" << &num1 << std::endl;
        func();
        num1++;
    }

    return 0;
}
```

**Capture by Reference**
```cpp
#include <iostream>

int main(int argc, char **argv) {
    int num1{42};
    double num2{12.6};

    // `&` syntax lets access outside this function
    auto func = [&](){
        std::cout << "Inner value (num1): " << num1 << std::endl;
        std::cout << "Inner value (num2): " << num2 << std::endl;
    };

    for (size_t i = 0; i < 3; i++) {
        std::cout << "\nOuter value (num1): " << num1 << std::endl;
        std::cout << "Outer value (num2): " << num2 << std::endl;
        func();
        num1++;
        num2 += 0.4;
    }

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/lambda