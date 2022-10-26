---
aliases:
---
**tags:** #C/Structures/Tags #C/Structures/Pointers #C/Pointers/Structures #C/Lecture  
**[[Cstructures|BACK]]**

---
## Accessing members of structure using structure pointer
```C
#include <stdio.h>

struct abc{
    int x;
    int y;
};

int main(){
    struct abc a = {0, 1};

    // ptr is pointer to some variable of type struct abc
    struct abc *ptr = &a;

    // ptr.x == (*ptr).x = (*&a).x = a.x
    printf("%d %d", ptr->x, ptr->y);
    return 0;
}
```

# 

<br>

---
**Source:**
- [Pointer to Structure Variable - YouTube](https://www.youtube.com/watch?v=VsnXsfNstVw&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=157)