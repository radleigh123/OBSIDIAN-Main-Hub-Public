---
aliases:
tags:
- CPP/Lecture
- CPP/Functions
- CPP/References
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## Input/Output parameters
**Output parameters** should be passed in such a way that you can modify the arguments from inside the functions. Options are passing by reference or by pointer. [[C++references|References]] are preferred in C++.

**Input parameters** shouldn't be modifiable from inside a function. The function really need to get input(read) from the arguments. You enforce modification restrictions with the `const` keyword. Options are passing by `const` reference, passing by pointer to `const`, or even passing by `const` pointer to const

**e.g.**
```cpp
#include <iostream>

void max_str(const std::string, const std::string, std::string &);
void max_int(int, int, int &);
void max_double(double, double, double *);

int main() {
    // max_str function
    std::string out_str;
    std::string str1("Alabamc");
    std::string str2("Alabamb");
    max_str(str1, str2, out_str);
    std::cout << "max_str: " << out_str << std::endl;

    // max_int function
    int out_int;
    int in1{205}, in2{155};
    max_int(in1, in2, out_int);
    std::cout << "max_int: " << out_int << std::endl;

    // max_double function
    double out_double;
    double dob1{45.23}, dob2{23.12};
    max_double(dob1, dob2, &out_double);
    std::cout << "max_double: " << out_double << std::endl;

    return 0;
}

void max_str(const std::string input1, const std::string input2, std::string &output) {
    if (input1 > input2) output = input1;
    else output = input2;
}

void max_int(int input1, int input2, int &output) {
    if (input1 > input2) output = input1;
    else output = input2;
}

void max_double(double input1, double input2, double *output) {
    if (input1 > input2) *output = input1;
    else *output = input2;
}
```