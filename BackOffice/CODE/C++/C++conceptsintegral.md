---
aliases:
tags:
- CPP/Lecture
- CPP/Library/concepts/integral
---
**[[C++|HOME [C++]]]**

---
## `integral<>`
The concept `integral<T>` is satisfied if and only if `T` is an integral type.
>[!column|clean no-t]
>>[!INFO|clean no-i collapse] **Syntax1**
>> ```cpp
>> template <typename T>
>> requires std::integral<T>
>> T add(T a, T b) {
>> 	return (a + b);
>> }
>> ```
>> <br>
>>
>> **Syntax2 \- using type traits**
>> ```cpp
>> template <typename T>
>> requires std::is_integral_v<T>
>> T add(T a, T b) {
>> 	return (a + b);
>> }
>> ```
>> <br>
>> 
>> **Syntax3**
>> ```cpp
>> template <std::integral T>
>> T add(T a, T b) {
>> 	return (a + b);
>> }
>> ```
>
>>[!INFO|clean no-i collapse] **Syntax4**
>> ```cpp
>> auto add(std::integral auto a, std::integral auto b) {
>> 	return (a + b);
>> }
>> ```
>> <br>
>> 
>> **Syntax5**
>> ```cpp
>> template <typename T>
>> T add(T a, T b) requires std::integral<T> {
>> 	return (a + b);
>> }
>> ```

<br>

**e.g.**
```cpp
#include <iostream>
#include <concepts>

auto add(std::integral auto a, std::integral auto b) {
    return a + b;
}

int main(int argc, char **argv) {
    char var_char1{10}, var_char2{20};
    auto result1{add(var_char1, var_char2)};
    std::cout << "result1: " << static_cast<int>(result1) << std::endl;

    int var_int1{11}, var_int2{15};
    auto result2{add(var_int1, var_int2)};
    std::cout << "result2: " << result2 << std::endl;

    /*
    // Error double is not integral
    double var_double1{15.33}, var_double2{25.33};
    auto result3{add(var_double1, var_double2)};
    std::cout << "result3: " << result3 << std::endl;
    */

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/concepts/integral