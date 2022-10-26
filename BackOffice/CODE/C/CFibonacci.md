---
aliases:
---
**tags:** #C/Loop 
**[[1ControlFlow|BACK]]**

---
```C
// Program to print Fibonacci series to a no. of terms
#include<stdio.h>
int main(){
    int num1;

    // initialize first and second terms
    int t1 = 0, t2 = 1;

    // initialize the next term (3rd term)
    int nextTerm = t1 + t2;

    // get no. of terms from the user
    printf("Enter the number of terms: ");
    scanf("%d", &num1);

    // print the first two terms t1 and t2
    printf("Fibonacci Series: %d, %d", t1, t2);

    // print 3rd to nth terms
    for (int i = 3; i < num1; i++){
        printf(", %d", nextTerm);
        t1 = t2;
        t2 = nextTerm;
        nextTerm = t1 + t2;
    }  

    return 0;
}
```