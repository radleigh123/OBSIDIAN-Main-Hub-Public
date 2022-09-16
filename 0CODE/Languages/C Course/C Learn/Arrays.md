#array

```C
// Basic Array syntax
#include<stdio.h>
int main(){
    // initializing array data
    int data[] = {45, 26, 89, 333, 78};

    // modifying array elements
    data[3] = 444;

    for (int i = 0; i <= 5; i++){
        printf("Index %d item: %d\n", i, data[i]);
    }
    
    return 0;
}
```