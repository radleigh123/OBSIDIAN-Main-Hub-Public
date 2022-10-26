---
aliases:
---
**tags:** #C/Strings 
**[[Cstrings|BACK]]**

---
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

```C
char string1[] = "Hello";
printf("%s\n", string1); // Hello

printf("%s\n", "You have to dream before your dreams can come true.\
--A.P.J. Abdul Kalam"); // Considers the 4 spaces before --

printf("%s\n", "You have to dream before your dreams can come true. "
"--A.P.J. Abdul Kalam"); // Does not consider indentation before --
```