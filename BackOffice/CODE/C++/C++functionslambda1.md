---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
---
**[[C++functionslambda|BACK]]**

---
## Lambda function sample 1
```cpp
#include <iostream>

int main(int argc, char **argv)
{
    [](double a, double b)
    {
        std::cout << "a + b = " << a + b;
    }(12.5, 5.3);

    return 0;
}
```