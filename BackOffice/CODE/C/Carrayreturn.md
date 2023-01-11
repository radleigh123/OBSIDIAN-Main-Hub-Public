---
aliases:
tags:
- C/Arrays/Functions
- C/Arrays/Pointers
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Return Array
An [[Carrays|array]] is a type of data structure that stores a fixed-size of a homogeneous collection of data. In short, we can say that array is a collection of variables of the same type.

**Passing array to a [[Cfunctions|function]]**
```C
#include <stdio.h>

void getarray(int arr[])
{
    printf("Elements of array are : ");

    for(int i=0;i<5;i++) printf("%d ", arr[i]);
}

int main()
{
   int arr[5]={45,67,34,78,90};
   getarray(arr);

   return 0;
}
```

**Returning array by passing an array which is to be returned as a parameter to the [[Cfunctions|function]]**
```C
#include <stdio.h>

int *getarray(int *a)
{
    printf("Enter the elements in an array:\n");
    for(int i=0;i<5;i++) scanf("%d", &a[i]);

    return a;
}

int main()
{
    int *n;
    int a[5];
    n=getarray(a);

    printf("\nElements of array are:\n");
    for(int i=0;i<5;i++) printf("%d\n", n[i]);

    return 0;
}
```

<br>

# 
---
**Sources:**
- [Passing Array to Function in C - javatpoint](https://www.javatpoint.com/passing-array-to-function-in-c)
- [Return an Array in C - javatpoint](https://www.javatpoint.com/return-an-array-in-c)