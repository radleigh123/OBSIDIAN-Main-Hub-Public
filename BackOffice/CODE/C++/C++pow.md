---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/pow
---
**[[C++mathfunctions|BACK]]**

---
## `std::pow`
raises a number to the given power ($x^y$)

```cpp
#include <iostream>
#include <cmath>

int main()
{
    std::cout << "3^4 is " << std::pow(3, 4) << std::endl;
    std::cout << "9^3 is " << std::pow(9, 3) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/pow