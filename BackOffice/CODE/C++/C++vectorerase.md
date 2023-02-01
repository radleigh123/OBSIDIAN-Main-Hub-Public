---
aliases:
tags:
- CPP/Library/vector/vector/erase
---
**[[C++vector|BACK]]**

---
## vector: erase
>[!aside|right]+ 
> 0 1 2 3 4 5 6 7 8 9
> 1 2 3 4 5 6 7 8 9
> 1 2 6 7 8 9
> 1 7 9

```cpp
#include <vector>
#include <iostream>
 
 
void print_container(const std::vector<int>& c) 
{
    for (int i : c)
        std::cout << i << " ";
    std::cout << '\n';
}
 
int main( )
{
    std::vector<int> c{0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    print_container(c);
 
    c.erase(c.begin());
    print_container(c);
 
    c.erase(c.begin()+2, c.begin()+5);
    print_container(c);
 
    // Erase all even numbers
    for (std::vector<int>::iterator it = c.begin(); it != c.end();)
    {
        if (*it % 2 == 0)
            it = c.erase(it);
        else
            ++it;
    }
    print_container(c);
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/container/vector/erase