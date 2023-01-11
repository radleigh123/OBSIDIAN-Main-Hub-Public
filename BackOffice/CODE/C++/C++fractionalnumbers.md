---
cssclass: t-c, tbl-nalt
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/setprecision
---
**[[C++|HOME [C++]]]**

---
## Fractional Numbers

| Type          | Size | Precision | Remark              |
| ------------- | ---- | --------- | ------------------- |
| `float`       | 4    | 7         |                     |
| `double`      | 8    | 15        | Recommended default |
| `long double` | 12   | >double   |                     |

**e.g.**
```cpp
#include <iostream>
#include <iomanip>

int main()
{
    float num1{15.2151561f}; // put 'f' to identify as float
    double num2{365.231565};
    long double num3{215.3515L}; // put 'L' to identify as long double

    std::cout << std::setprecision(8); // Control precision from std::cout
    std::cout << "Number1 = " << num1 << std::endl;
    std::cout << "Number2 = " << num2 << std::endl;
    std::cout << "Number3 = " << num3 << std::endl;

    return 0;
}
```

**Scientific Notations**
```cpp
#include <iostream>

int main()
{
    double num1{3.498e-11}; // scientific notation

    std::cout << num1 << std::endl;
    return 0;
}
```