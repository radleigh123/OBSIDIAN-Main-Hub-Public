```C
// Program to print ASCII value
#include<stdio.h>
int main(){
    char char1;
    printf("Enter a character: ");
    scanf("%c", &char1);

    // %c displays the actual character
    // %d displays the integer value of a character
    printf("\nASCII value of '%c': %d", char1, char1);

    return 0;
}
```