---
aliases:
tags:
- CPP/Library/vector/vector/insert
---
**[[C++vector|BACK]]**

---
## vector: insert
>[!aside|right]+ 
> 1. 100 100 100
> 2. 200 100 100 100
> 3. 300 300 200 100 100 100
> 4. 300 300 400 400 200 100 100 100
> 5. 501 502 503 300 300 400 400 200 100 100 100
> 6. 501 502 503 300 300 400 400 200 100 100 100 601 602 603

```cpp
#include <iostream>
#include <iterator>
#include <vector>

// function to print the vector elements in the given range
void print(int id, const std::vector<int> &container) {
    std::cout << id << ". ";
    for (const int x : container) std::cout << x << ' ';
    std::cout << '\n';
}

int main() {
    // create a vector of size 3 with all elements having value 100
    std::vector<int> c1(3, 100);
    print(1, c1);

    // insert a value of 200 at the beginning of the vector
    auto it = c1.begin();
    it = c1.insert(it, 200);
    print(2, c1);

    // insert 2 values of 300 at the position of the iterator
    c1.insert(it, 2, 300);
    print(3, c1);

    // `it` no longer valid, get a new one:
    it = c1.begin();

    // create a new vector with 2 values of 400
    std::vector<int> c2(2, 400);
    // insert the entire c2 vector into c1 at position of 2nd element
    c1.insert(std::next(it, 2), c2.begin(), c2.end());
    print(4, c1);

    // create an array with values 501, 502, 503
    int arr[] = {501, 502, 503};
    // insert the entire array into c1 at the beginning
    c1.insert(c1.begin(), arr, arr + std::size(arr));
    print(5, c1);

    // insert values 601, 602, 603 at the end of c1
    c1.insert(c1.end(), {601, 602, 603});
    print(6, c1);
}
```
The above code demonstrates the use of the `insert` function of the `std::vector` class. This function is used to insert elements into a vector at a specified position. The first argument to the function is an iterator pointing to the position where the new elements will be inserted.

It also uses `std::next` to move the iterator to a specific position and `std::size()` to get the size of array elements. The `auto` keyword is used to deduce the iterator type, in this case, it will be deduced as `std::vector<int>::iterator`.

The function demonstrates several ways to insert elements into a vector, including inserting a single value, inserting a number of copies of a value, inserting elements from another container, and inserting elements from an array or initializer list. It also uses the function `print` to print the vector element each time the insert function is called to show the changes in the vector.

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/container/vector/insert