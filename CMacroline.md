#C #Cmacros #Cstrings 

```C
#include<stdio.h>
int main(){
    printf("Hello world\t");
    printf("Line in the source file: %d\n", __LINE__ - 1);

    printf("How are you?\t");
    printf("Line in the source file: %d", __LINE__ - 1);

    printf("\n\nBye!!!");

    return 0;
}
// is a preprocessor macro that expands to current line number in the source file, as an integer. 
// useful when generating log statements, error messages intended for programmers.

// can find current line number in source file.
```