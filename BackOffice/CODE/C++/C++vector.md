---
cssclass: s-li
aliases:
tags:
- CPP/Lecture
- CPP/Library/vector/vector
---
**[[C++|HOME [C++]]]**

---
## `std::vector`
is a container class in the C++ Standard Template Library (STL). It is <mark class="hltr-blue">similar to an array but it can grow or shrink in size dynamically</mark>, which means that you can add or remove elements from a vector after it is created.

>[!INFO|alt-co]+ Ways of declaring a vector:
> - **initializer list** - `std::vector<int> v = {1, 2, 3, 4, 5};`
> - std::vector **constructor** - `std::vector<int> v(5);`
> 	- `std::vector<int> v(5, 2);`  all initialized to 2
> - **iterators** - `std::vector<int> v(v1.begin(), v1.end());` creates a new vector, v, with the same elements as an existing vector v1.
> - **emplace_back function** creates a new instance of *MyClass* with arg1 and arg2 inside the vector
> ```cpp
> std::vector<myClass> v;
> v.emplace_back(arg1, arg2);
> ```

**e.g.**
```cpp
#include <iostream>
#include <vector>

int main() {
    // Create an empty vector of integers
    std::vector<int> v;

    // Manually add elements
    v.push_back(1);
    v.push_back(2);
    v.push_back(3);

    for (int i : v) { std::cout << i << " "; } // 1 2 3
    std::cout << std::endl;

    v.pop_back(); // Remove the last element

    for (int i : v) { std::cout << i << " "; } // 1 2
    std::cout << std::endl;

    v.resize(5); // resize the vector

    for (int i : v) { std::cout << i << " "; } // 1 2 0 0 0
    std::cout << std::endl;

    v.clear(); // clear the vector

    for (int i : v) { std::cout << "This will not print, `v` is now empty."; } // 
    std::cout << std::endl;

    return 0;
}
```
>[!FAQ|alt-co]+ Modifiers
> **clear** - clears the contents
> **[[C++vectorinsert|insert]]** - inserts elements
> **emplace** C++11 - constructs element in-place
> **[[C++vectorerase|erase]]** - erases elements
> **push_back** - adds an element to the end
> **emplace_back** C++11 - constructs an element in-place at the end
> **pop_back** - removes the last element
> **resize** - changes the number of elements stored
> **[[C++vectorswap|swap]]** - swaps the contents

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/container/vector