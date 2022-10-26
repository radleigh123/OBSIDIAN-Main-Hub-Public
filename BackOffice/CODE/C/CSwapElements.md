---
aliases:
---
**tags:** #C/Arrays/Functions  
**[[1ArrayPointers|BACK]]**

---
```C
// Program to swap elements using call by reference
#include<stdio.h>

void cyclicSwap(int *a, int *b, int *c);

int main(){
    int a, b, c;

    printf("Enter a, b, and c respectively: ");
    scanf("%d%d%d", &a, &b, &c);

    printf("Value before swapping:\n");
    printf("a = %d\tb = %d\tc = %d", a, b, c);

    // addresses of the numbers are passed to the cyclicSwap() function
    cyclicSwap(&a, &b, &c);

    printf("\nValue after swapping:\n");
    printf("a = %d\tb = %d\tc = %d", a, b, c);

    return 0;
}

void cyclicSwap(int *num1, int *num2, int *num3){
    int temp;

    // swapping in cyclic order
    temp = *num2;
    *num2 = *num1;
    *num1 = *num3;
    *num3 = temp;
}
```