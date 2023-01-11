---
aliases:
tags:
- CPP/Lecture
- CPP/Library/cmath/log
---
**[[C++mathfunctions|BACK]]**

---
## `std::log`
computes natural (base $e$) logarithm ($lnx$)
>[!NOTE]+
>- **log** - reverse function of [[C++pow|`pow`]]. If $2^3$ = 8, log 8 in base 2 = 3. Log is like asking
>	- to which exponent should we elevate 2 to get eight ? Log, by default computes the log
>	- in base $e$. There also is another function which uses base 10 called `log10`

<br>

**e.g.**
```cpp
#include <iostream>
#include <cmath>

int main()
{   
    // e^4 = 54.59, it will be log 54.59 in base e = ?
    std::cout << "Log ; to get 54.59, you should elevate e to the power of: " << std::log(54.59) << std::endl;

    // log10, 10^4 = 10000, to get 10k, you'd need to elevate 10 to the power of ?, this is log in base 10
    std::cout << "To get 1000, you'd need to elevate 10 to the power of: " << std::log10(10000) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/numeric/math/log