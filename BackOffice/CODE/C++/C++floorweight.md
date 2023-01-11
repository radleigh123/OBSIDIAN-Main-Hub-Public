---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/floor
- CPP/Library/cmath/ceil
---
**[[C++mathfunctions|BACK]]**

---
## `std::floor` `std::weight`
**floor** - nearest integer not greater than the given value
**ceil** - nearest integer not less than the given value

```cpp
#include <iostream>
#include <cmath>

int main()
{
    double weight{10.45};

    // floor
    std::cout << "Weight rounded to floor: " << std::floor(weight) << std::endl;

    // ceil
    std::cout << "Weight rounded to ceil: " << std::ceil(weight) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/floor
- https://en.cppreference.com/w/cpp/numeric/math/ceil