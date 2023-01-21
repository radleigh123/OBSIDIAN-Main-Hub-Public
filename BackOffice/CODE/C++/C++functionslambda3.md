---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
- CPP/Conversion
---
**[[C++functionslambda|BACK]]**

---
## Lambda function sample 3
```cpp
#include <iostream>

int main(int argc, char **argv) {
    // Explicitly converting double vars into `int`
    auto func = [](double a, double b) -> int{
        return (a + b);
    };
    
    auto func1 = [](double a, double b) {
        return (a + b);
    };

    std::cout << func(5.1234, 1.3215) << std::endl;
    std::cout << func1(5.1234, 1.3215) << std::endl;

    std::cout << "\nSuccessfully called lambda function!";
    return 0;
}
```