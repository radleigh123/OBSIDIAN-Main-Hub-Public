---
aliases:
---
**tags:** #C/Loop #C/Functions/Recursion 
**[[1ControlFlow|BACK]]**

---
```C
// Program to find the factorial of a number
#include<stdio.h>
int main(){
    int num1;
    unsigned long long fact = 1;
    printf("Enter an integer: ");
    scanf("%d", &num1);

    // shows error if the user enters a negative integer
    if (num1 < 0){
        printf("Error! Factorial of a negative number doesn't exist");
    } else
    {
        for (int i = 1; i <= num1; i++){
            fact *= i;
        }
        printf("Factorial of %d: %llu", num1, fact);
    }
    
    return 0;
}
```

```C
// Factorial of a Number using recursion
#include<stdio.h>
long int multiplyNumbers(int n);
int main() {
    int n;
    printf("Enter a positive integer: ");
    scanf("%d",&n);
    printf("Factorial of %d = %ld", n, multiplyNumbers(n));
    return 0;
}

long int multiplyNumbers(int n) {
    if (n>=1)
        return n*multiplyNumbers(n-1);
    else
        return 1;
}
```