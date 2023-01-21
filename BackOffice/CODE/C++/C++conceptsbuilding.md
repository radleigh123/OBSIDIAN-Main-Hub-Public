---
aliases:
tags:
- CPP/Lecture
- CPP/Library/concepts/integral
- CPP/Library/concepts/is_integral_v
- CPP/Library/type_traits
---
**[[C++|HOME [C++]]]**

---
## Concepts: Building your own
requires the template parameter to satisfy the concept used, else it will give error to the compiler like a failsafe

>[!column|collapse ttl-c clean no-t]
>>[!INFO|clean no-i] Standard built-in concepts
>
>>[!INFO|clean no-i] <mark class="hltr-blue">Custom concepts</mark>

>[!column|ttl-c no-t] Different ways to build concepts
>>[!INFO|clean no-t]
>> **Ways of building concepts:**
>> ```cpp
>> template <typename T>
>> concept myIntegral = std::is_integral_v<T>;
>> ```
>>
>> ```cpp
>> template <typename T>
>> concept multiply = requires(T a, T b) { a * b; };
>> ```
>
>>[!INFO|clean no-t]
>> &nbsp
>> ```cpp
>> // requires parameter to be incrementable
>> template <typename T>
>> concept increment = requires(T a) {
>> 						a += 1;
>> 						++a;
>> 						a++;
>> 					};
>> ```

>[!column|ttl-c no-t] Different ways to build concepts
>>[!INFO|clean no-t]
>> **Syntax**
>> ```cpp
>> template <typename T>
>> requires myIntegral<T>
>> T add_1(T a, T b) { return (a + b); }
>> ```
>>
>> ```cpp
>> template <typename T>
>> T add_2(T a, T b) { return (a + b); }
>> ```
>
>>[!INFO|clean no-t]
>> &nbsp
>> ```cpp
>> auto add_3(myIntegral auto a, myIntegral auto b) { return (a + b); }
>> ```

---
**e.g. 1**
```cpp
#include <iostream>
#include <concepts>
#include <type_traits> // optional

template <typename T>
concept myIntegral = std::is_integral_v<T>;

template <typename T>
requires myIntegral<T>
T add(T a, T b) { return (a + b); }

int main(int argc, char **argv) {
    int num1{15}, num2{5};

    std::cout << add(num1, num2);

    return 0;
}
```
**e.g. 2**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept multiply = requires(T a, T b) { a *b; };

template <typename T>
    requires multiply<T>
T add(T a, T b) { return (a + b); }

int main(int argc, char **argv) {
    double num1{15.55}, num2{5.1};
    std::cout << add(num1, num2);

    // ERROR! strings is not capable of multiplying
    std::string str1{"hello"}, str2{"world"};
    std::cout << add(str1, str2);

    return 0;
}
```
**e.g. 3**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept increment = requires(T a) {
                        a += 1;
                        ++a;
                        a++;
                    };

template <typename T>
requires increment<T>
T add(T a, T b) { return (a + b); }

int main(int argc, char **argv) {
    double num1{15.55}, num2{6.1};

    std::cout << add(num1, num2);

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/types/is_integral