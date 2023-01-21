---
aliases:
tags:
- CPP/Lecture
- CPP/References
- CPP/Functions/template
- CPP/const
---
**[[C++|HOME [C++]]]**

---
## Template type parameters by Reference
**template type parameters by value**
```cpp
#include <iostream>

template <typename T> T maximum(T a, T b);

int main(int argc, char **argv) {
    double var1{45.66}, var2{55.12};

    std::cout << "Out - &a: " << &var1 << std::endl;
    double max1 = maximum(var1, var2);
    std::cout << "\nmax1: " << max1 << std::endl;

    return 0;
}

template <typename T>
T maximum(T a, T b) {
    std::cout << "In - &a: " << &a << std::endl;
    return (a > b) ? a : b;
}
```

<br>

**template type parameters by reference**
```cpp
#include <iostream>

template <typename T> const T &maximum(const T &a, const T &b);

int main(int argc, char **argv) {
    double var1{45.66}, var2{55.12};

    std::cout << "Out - &a: " << &var1 << std::endl;
    double max1 = maximum(var1, var2);
    std::cout << "\nmax1: " << max1 << std::endl;

    return 0;
}

template <typename T>
const T &maximum(const T &a, const T &b) {
    std::cout << "In - &a: " << &a << std::endl;
    return (a > b) ? a : b;
}
```

>[!FAIL|alt-co]+ Confusing your compiler
> ```cpp
> #include <iostream>
> 
> template <typename T> T maximum(T a, T b);
> template <typename T> const T &maximum(const T &a, const T &b);
> 
> int main(int argc, char **argv) {
> 	double var1{45.66}, var2{55.12};
> 	
> 	std::cout << "Out - &a: " << &var1 << std::endl;
> 	double max1 = maximum(var1, var2);
> 	std::cout << "\nmax1: " << max1 << std::endl;
> 	
> 	return 0;
> }
> 
> template <typename T> T maximum(T a, T b) {
> 	return (a > b) ? a : b;
> }
> 
> template <typename T> const T &maximum(const T &a, const T &b) {
> 	std::cout << "In - &a: " << &a << std::endl;
> 	return (a > b) ? a : b;
> }
> ```