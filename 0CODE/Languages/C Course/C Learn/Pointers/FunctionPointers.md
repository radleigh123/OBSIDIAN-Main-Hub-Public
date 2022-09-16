#Cpointers #Cfunctions

```C
#include<stdio.h>

void addOne(int *pc){
    (*pc)++;
}

int main(){
    int *p, i = 10;
    
    // assigning &i address to p
    p = &i;
    // address of p is passed
    addOne(p);

    printf("%d", *p);
    return 0;
}
```