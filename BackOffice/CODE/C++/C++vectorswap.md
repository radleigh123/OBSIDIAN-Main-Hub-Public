---
aliases:
tags:
- CPP/Library/vector/vector/swap
---
**[[C++vector|BACK]]**

---
## vector: swap
>[!aside|right]+ 
> { 1 2 3 } { 4 5 } 2 5 1 4
> { 4 5 } { 1 2 3 } 2 5 1 4

```cpp
#include <iostream>
#include <vector>
 
template<class Os, class Co>
Os& operator<<(Os& os, const Co& co) {
    os << "{";
    for (auto const& i : co) os << ' ' << i;
    return os << " } ";
}
 
int main() {
    std::vector<int> a1{1, 2, 3}, a2{4, 5};
 
    // This will create two iterators, it1 will point to the 2nd element of a1 and it2 will point to the 2nd element of a2
    auto it1 = std::next(a1.begin());
    auto it2 = std::next(a2.begin());
 
    // This will create two references, ref1 will refer to the first element of a1 and ref2 will refer to the first element of a2
    int& ref1 = a1.front();
    int& ref2 = a2.front();
 
    // This line will print the current values of a1, a2, *it1, *it2, ref1, ref2
    // *it1 and *it2 will dereference the iterators to get the values they are pointing to
    std::cout << a1 << a2 << *it1 << ' ' << *it2 << ' ' << ref1 << ' ' << ref2 << '\n';
 
    // This will swap the contents of a1 and a2
    a1.swap(a2);
 
    // This line will print the new values of a1, a2, *it1, *it2, ref1, ref2
    // Note that the values of the iterators and references will not change 
    // even though the contents of the vectors were swapped
    std::cout << a1 << a2 << *it1 << ' ' << *it2 << ' ' << ref1 << ' ' << ref2 << '\n';
}
```
This code will print the values of two vectors `a1` and `a2`, two iterators `it1` and `it2`, and two references `ref1` and `ref2` before and after swapping the contents of the vectors. 

The function `std::next(a1.begin())` will return an iterator pointing to the next element of a1 after the first element, it is used here to move the iterator to the second element of the vector.

`a1.front()` is used to get the first element of the vector, and `a2.front()` for the second. `std::cout << a1 << a2 << *it1 << ' ' << *it2 << ' ' << ref1 << ' ' << ref2 << '\n';` will print the values of the vectors, the values pointed to by the iterators and the values referred to by the references.

`a1.swap(a2)` will swap the contents of the two vectors. It is important to note that after the swap, the iterators and references will stay associated with their original elements, meaning `it1` will still point to the same element it did before the swap, even though this element is now in a2.

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/container/vector/swap