```C
// Program to Check alphabet
#include<stdio.h>
int main(){
    char char1;
    printf("Enter a character: ");
    scanf("%c", &char1);

    if ((char1 >= 'a' && char1 <= 'z') || (char1 >= 'A' && char1 <= 'Z')){
        printf("%c is an alphabet", char1);
    } else{
        printf("%c is not an alphabet!");
    }
    
    return 0;
}
```