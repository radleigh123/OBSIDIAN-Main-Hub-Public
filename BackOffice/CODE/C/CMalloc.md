---
aliases:
---
**tags:** #C/Miscellaneous/Memory_Allocation #C/Miscellaneous/Memory_Allocation/malloc #C/Miscellaneous/Memory_Allocation/free  
**[[0Memory Allocation|BACK]]**

---
## Malloc
```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int num1 = 100;
    double *pointer;
    
    printf("Size of Double: %lu\n", sizeof(double));

    // statement allocates 800 bytes of memory. Double is 8bytes
    // And, Pointer holds the address of the first byte in the allocated memory
    pointer = (double*) malloc(num1 * sizeof(double));

    return 0;
}
```

## MallocFree
```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int *pointer, num1, sum = 0;
    printf("Enter number of elements: ");
    scanf("%d", &num1);

    pointer = (int*) malloc(num1 * sizeof(int));

    // if memory cannot be allocated
    if(pointer == NULL){
        printf("Error! memory not allocated.");
        exit(0);
    }

    printf("Enter elements: ");
    for (int i = 0; i < num1; i++){
        scanf("%d", pointer + i);
        sum += *(pointer + i);
    }
    
    printf("Sum = %d", sum);

    // deallocating the memory
    free(pointer);

    return 0;
}
```