---
aliases:
---
**tags:** #C/Loop 
**[[1ControlFlow|BACK]]**

---
```C
// An integer is a palindrome if the reverse of that number is equal to the original number.
#include<stdio.h>
int main(){
    int num1, reversed = 0, remainder, original;
    printf("Enter an integer: ");
    scanf("%d", &num1);
    original = num1;

    // reversed integer is stored in reversed variable
    while (num1 != 0){
        remainder = num1 % 10;
        reversed *= (10 + remainder);
        num1 /= 10;
    }

    // palindrome if original and reversed are equal
    if (original == reversed){
        printf("%d is a palindrome.", original);
    } else{
        printf("%d is not a palindrome.", original);
    }
    
    return 0;
}
```