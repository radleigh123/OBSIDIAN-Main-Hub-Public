```C
// Program to remove characters in string except alphabets
#include<stdio.h>

int main(){
    char string[150];

    printf("Enter a string: ");
    fgets(string, sizeof(string), stdin);

    for (int i = 0, j; string[i] != '\0'; i++){
        // enter the loop if the character is not an alphabet
        // and not null character
        while (!(string[i] >= 'a' && string[i] <= 'z') && !(string[i] >= 'A' && string[i] <= 'Z') && !(string[i] == '\0')){
            for (j = i; string[j] != '\0'; j++){
                // if jth element of string is not an alphabet
                // assign the value of (j+1)th element to the jth element
                string[j] = string[j + 1];
            }
            string[j] = '\0';
        }
    }
    
    printf("Outpout string: ");
    puts(string);
    
    return 0;
}
```