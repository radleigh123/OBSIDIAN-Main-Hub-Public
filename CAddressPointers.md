#C #Cpointers 

```C
#include<stdio.h>
int main(){
    int *pc, var = 10, var2 = 15;
    
    // &var means its address not the value itself. REMEMBER!!!
    pc = &var;

    // Notice the use of * before pc in getting the value NOT THE ADDRESS
    printf("Value of var: %d\tValue of pc: %d\n", var, *pc);
    // Notice the use of & before var in GETTING THE ADDRESS
    printf("Address of var: %p\n", &var);

    printf("\n-----------------------------------\n\n");

    // Both are the same in changing values because PC and ADDRESS OF VAR ARE THE SAME
    var = 1;
    *pc = 20;
    
    printf("Value of var: %d\tValue of pc: %d\n", var, *pc);
    printf("Address of var: %p\n", &var);

    printf("\n-----------------------------------\n\n");

    // Testing another VAR2 with same PC
    pc = &var2;
    var2 = 50;

    printf("Value of var2: %d\tValue of pc: %d\n", var2, *pc);
    printf("Address of var2: %p\n", &var2);

    return 0;
}
```