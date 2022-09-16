#C #Cmacros 

```C
// used to confirm the compiler standard. Generally it holds the value 1 
// which means that the compiler conforms to ISO Standard C

#include<stdio.h>
int main(){
    printf("Compiler Standard Number: %d", __STDC__);

    return 0;
}
```