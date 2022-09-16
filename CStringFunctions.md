#C #Cstrings  #Cfunctions  #Cfgets #Cputs

```C
#include<stdio.h>
void displayString(char name[]);

int main(){
    char name[30];
    printf("Enter string: ");

    fgets(name, sizeof(name), stdin);
    displayString(name);

    return 0;
}

void displayString(char name[]){
    printf("String Output: ");
    puts(name);
}
```