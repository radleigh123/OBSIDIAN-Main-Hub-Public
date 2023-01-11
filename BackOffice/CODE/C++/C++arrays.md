---
title: C++declaringarrays
creation-date: 2023-01-09
aliases:
tags:
- CPP/Lecture
- CPP/Arrays
- CPP/FlowControl/rangefor
- CPP/const
---
**[[C++|HOME [C++]]]**

---
# Declaring and using array
```cpp
#include <iostream>

int main() {
    // Declaring an array
    int arr1[]{1, 2, 8, 9, 5}; // or int arr1[5]{1, 2, 8, 9, 5};
	
	// Writing data in an array
    arr1[4] = 20;

    // Reading values
    for (size_t i = 0; i < 5; i++) {
        std::cout << arr1[i] << " ";
    }

    return 0;
}
```

**Using for range loop**
```cpp
#include <iostream>

int main() {
    int arr1[]{10, 20, 30, 40, 50};

    for (auto &i : arr1) {
        std::cout << i + 5 << std::endl;
    }

    return 0;
}
```

**Constant array**
```cpp
#include <iostream>

int main() {
    const int arr1[]{21, 22, 23};

    arr1[2] = 20; // ERROR: cant modify element of const array

    return 0;
}
```

<br>

# 
---
**Sources:**
- **std::array** - https://en.cppreference.com/w/cpp/container/array