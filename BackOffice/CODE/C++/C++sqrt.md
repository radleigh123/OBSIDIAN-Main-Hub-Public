---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/sqrt
- CPP/Library/cmath/round
---
**[[C++mathfunctions|BACK]]**

---
## `std::sqrt`
computes square root ($√x$)

```cpp
#include <iostream>
#include <cmath>

int main()
{
    // sqrt
    std::cout << "The square root of 36 is: " << std::sqrt(36) << std::endl;

    // round. Halfway points are rounded away from 0
    std::cout << "3.654 rounded to " << std::round(3.654) << std::endl;
    std::cout << "2.5 rounded to " << std::round(2.5) << std::endl;
    std::cout << "2.4 rounded to " << std::round(2.4) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/sqrt