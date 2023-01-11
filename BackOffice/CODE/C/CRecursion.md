---
aliases:
tags:
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Recursion
is the process which comes into existence when a function calls a copy of itself to work on a smaller problem
```C
#include <stdio.h>
int fact (int);

int main()
{
    int n,f;
    printf("Enter the number whose factorial you want to calculate?");
    scanf("%d",&n);
    
    f = fact(n);
    printf("factorial = %d",f);

    return 0;
}

int fact(int n)
{
    if (n==0) return 0;
    else if ( n == 1) return 1;
    else return n*fact(n-1);
}
```
![[Pasted image 20230104154259.png|center]]

<br>

# 
---
**Sources:**
- [Recursion in C - javatpoint](https://www.javatpoint.com/recursion-in-c)