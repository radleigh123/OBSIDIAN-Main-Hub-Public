```C
#include<stdio.h>
int main(){
    FILE *ptr;
    int c;

    // open the current input file
    ptr = fopen(__FILE__, "r");

    do
    {
        c = getc(ptr); // read character
        putchar(c); // display character
    } while (c != EOF); // loop until the end of file is reached
    
    fclose(ptr);
    return 0;
}
```