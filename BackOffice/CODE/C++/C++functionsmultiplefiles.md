---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
- CPP/Preprocessor
---
**[[C++|HOME [C++]]]**

---
## Functions across multiple files
**main file:** `PROTO1.cpp`
```cpp
#include <iostream>
#include "comp.h" // Preprocessor/Directive
#include "ops.h"

int main() {
    int main_max{max(334, 56)};
    std::cout << "Maximum: " << main_max << std::endl;

    int main_min{min(334, 56)};
    std::cout << "Minimum: " << main_min << std::endl;

    std::cout << "\nIncremented result: " << incr_mult(5, 10);

    return 0;
}
```

>[!column|no-t]
>>[!INFO|clean no-i] **comp header file:** `comp.h`
>> ```cpp
>> int max(int, int);
>> int min(int, int);
>> ```
>> **comp file:** `comp.cpp`
>> ```cpp
>> int max(int a, int b) {
>> 	if (a > b) return a;
>> 	else return b;
>> }
>> 
>> int min(int a, int b) {
>> 	if (a < b) return a;
>> 	else return b;
>> }
>> ```
>
>>[!INFO|clean no-i] **ops header file:** `ops.h`
>> ```cpp
>> int incr_mult(int, int);
>> 
>> ```
>> **ops file:** `ops.cpp`
>> ```cpp
>> int incr_mult(int a, int b) {
>> 	return ((a++) * (++b));
>> }
>> ```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/preprocessor