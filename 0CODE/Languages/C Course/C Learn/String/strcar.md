#Cstrings

```C
#include<stdio.h>
#include<string.h>
int main(){
    char name1[100] = "This is ", name2[] = "Anjo World!";

    // concatenates NAME1 and NAME2
    // the resultant string is stored in NAME1
    strcat(name1, name2);
    // the size of the destination string should be large enough to store
    // the resultant string. If not, we will get the segmentation fault error.

    puts(name1);
    puts(name2);

    return 0;
}
```