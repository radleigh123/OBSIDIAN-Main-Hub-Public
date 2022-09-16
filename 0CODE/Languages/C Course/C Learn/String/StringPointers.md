#Cstrings #Cpointers 

```C
#include<stdio.h>
int main(){                
    char name[] = "Hairy Panther";
    /* 
    name[] = {'H', 'a', 'i', 'r', 'y', ' ',
              'P', 'a', 'n', 't', 'h', 'e', 'r', '/0'};
    */

    printf("%c", *name);
    printf("%c", *(name + 1));
    printf("%c\n", *(name + 12));

    char *namePTR;
    namePTR = name;

    printf("%c", *namePTR);
    printf("%c", *(namePTR + 1));
    printf("%c", *(namePTR + 12));

    return 0;
}
```