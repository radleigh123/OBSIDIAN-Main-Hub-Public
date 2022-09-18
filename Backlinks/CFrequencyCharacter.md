#C #Cstrings #Cloop 

```C
#include<stdio.h>

int main(){
    char string[1000], char1;
    int count = 0;

    printf("Enter a string: ");
    fgets(string, sizeof(string), stdin);

    printf("Enter a character to find its frequency: ");
    scanf("%c", &char1);

    for (int i = 0; string[i] != '\0'; i++){
        if (char1 == string[i]){
            count++;
        }
    }
    
    printf("Frequency of %c = %d", char1, count);

    return 0;
}
```