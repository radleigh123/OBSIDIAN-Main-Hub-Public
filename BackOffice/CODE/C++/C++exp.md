---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/exp
---
**[[C++mathfunctions|BACK]]**

---
## `std::exp`
returns $e$ raised to the given power ($e^x$)

```cpp
#include <iostream>
#include <cmath>

int main()
{
    // var1: f(x) = e^x, where e = 2.71828
    double var1 = std::exp(10);

    std::cout << "The exponential of 10 is: " << var1 << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/exp