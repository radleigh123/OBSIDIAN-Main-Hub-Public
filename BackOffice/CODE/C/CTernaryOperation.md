---
aliases:
---
**tags:** #C/Miscellaneous/Ternary 
**[[1ETCCODES|BACK]]**

---
## Ternary Operation
```C
#include<stdio.h>

int main(){
    int num1;
    printf("Enter a number: ");
    scanf("%d", &num1);

    // the same as... 
    /* if(num1 % 2 == 0){
        printf("%d is an even number.", num1);
    } else{
        printf("%d is an odd number." num1);
    } */
    (num1 % 2 == 0) ? printf("%d is an even number.", num1) : printf("%d is an odd number.", num1);

    return 0;
}
```