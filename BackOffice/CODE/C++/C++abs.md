---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/abs
---
**[[C++mathfunctions|BACK]]**

---
## `std::abs`
absolute value of a floating point value ($|x|$)

```cpp
#include <iostream>
#include <cmath>

int main()
{
    // abs
    double savings{-5000};

    std::cout << "Abs of savings is: " << std::abs(savings) << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/fabs