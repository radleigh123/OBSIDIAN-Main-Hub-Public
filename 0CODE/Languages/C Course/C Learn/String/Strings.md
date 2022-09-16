#Cstrings #Cfgets #Cputs 

```C
#include<stdio.h>

int main(){
    char name[30];

    // fgets() function to read a line of string even after WHITESPACE
    // puts() to display string
    printf("Enter name: ");
    fgets(name, sizeof(name), stdin); // reads string

    printf("My name is ");  
    puts(name); // display string


    // Notice the NAME without the '&'
    // because NAME is a char array, arrays decay into pointers in C
    printf("Enter name: ");
    scanf(" %[^\n]s", name); // for scanf to read the newLine

    printf("My name is %s.\n", name);

    return 0;
}
```