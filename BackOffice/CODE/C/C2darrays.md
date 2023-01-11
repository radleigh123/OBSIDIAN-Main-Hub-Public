---
aliases:
tags:
- C/Arrays/2D
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Two Dimensional Array
is organized as matrices which can be represented as the collection of rows and columns.
**Syntax:** `data_type array_name[rows][columns];`
```C
#include<stdio.h>

int main(){  
    int i=0,j=0;
    int arr[4][3]={
        {1,2,3}, 
        {2,3,4}, 
        {3,4,5}, 
        {4,5,6}}; 
    
    //traversing 2D array
    for(i=0;i<4;i++){
        for(j=0;j<3;j++){
            printf("arr[%d] [%d] = %d \n",i,j,arr[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

<br>

# 
---
**Sources:**
- [Two Dimensional Array in C - javatpoint](https://www.javatpoint.com/two-dimensional-array-in-c)