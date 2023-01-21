---
aliases:
tags:
- CPP/Lecture
- CPP/requires
- CPP/Library/concepts/convertible_to
- CPP/noexcept
- 
---
**[[C++requires|BACK]]**

---
## `requires`: Compound requirement
```cpp
template <typename T>
concept Addable = requires(T a, T b) {
	// noexcept is optional
	{a + b} noexcept -> std::convertible_to<int>;
	// Checks if `a + b` is valid syntax, doesn't throw expetions(optional),
	// and the result is convertible to int(optional).
};
```
<br>

---
**Returns false, `std::string` is not convertible to `int`**
```cpp
#include <iostream>
#include <concepts>

template <typename T>
concept addable = requires(T a, T b) { 
    { a + b } noexcept -> std::convertible_to<int>;
};

addable auto add(addable auto a, addable auto b) { return (a + b); }

int main(int argc, char **argv) {
    std::string var1{"hello"}, var2{"world"};

    auto result{add(var1, var2)};
    std::cout << "result: " << result << std::endl;
    std::cout << "sizeof(result): " << sizeof(result) << std::endl;

    return 0;
}
```

<br>

# 
---
**Sources:**
- **noexcept** - https://en.cppreference.com/w/cpp/language/noexcept
- **convertible_to** - https://en.cppreference.com/w/cpp/concepts/convertible_to