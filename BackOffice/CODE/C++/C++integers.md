---
aliases:
tags:
- CPP/Lecture
- CPP/Conversion/Typecasting
- CPP/Conversion/Narrowing_conversion
---
**[[C++|HOME [C++]]]**

---
## Integers
```cpp
#include<iostream>

int main()
{
    int first_num; // Variable declaration

    int second_num{}; // Variable initialization to 0

    int third_num{10}; // Variable initialization to 10

    // Can use expression as initializer
    int fourth_num{second_num + third_num};

	// Converts `double` into `int`
	// or narrowing_conversion{(int)215.145}
	// or narrowing_conversion = 215.145
	int narrowing_conversion(215.145);

    return 0;
}
```

>[!FAIL|alt-co txt-c]+ The expression uses undeclared variables
> ```cpp
> int fifth_num{a + b};
> ```

>[!FAIL|alt-co txt-c]+ Wrong data type used
> ```cpp
> int sixth_num{15.65};
> ```