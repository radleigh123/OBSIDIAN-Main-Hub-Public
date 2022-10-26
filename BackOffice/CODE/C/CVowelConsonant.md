---
aliases:
---
**tags:** #C/Strings/Loops #C/ctype 
**[[1Strings|BACK]]**

---
```C
// Program to count vowels, consonants, etc.
#include<stdio.h>
#include<ctype.h>

int main(){
    char string[150];
    int vowel, consonant, digit, space;

    // initialize all variables to 0
    vowel = consonant = digit = space = 0;

    // get full line of string input
    printf("Enter a line of string: ");
    fgets(string, sizeof(string), stdin);

    // loop through each character of the string
    for (int i = 0; string[i] != '\0'; i++){
        string[i] = tolower(string[i]); // conver character to lowercase

        // check if character is a vowel
        if (string[i] == 'a' || string[i] == 'e' || string[i] == 'i' || string[i] == 'o' || string[i] == 'u'){
            vowel++;
        } else if (string[i] >= 'a' && string[i] <= 'z'){
            // if it is not a vowel and if it is an alphabet, it is a consonant
            consonant++;
        } else if (string[i] >= '0' && string[i] <= '9'){
            // check if character is a digit
            digit++;
        } else if (string[i] == ' '){
            // check if character is an empty space
            space++;
        }
    }
    
    printf("Vowels: %d\t", vowel);
    printf("Consonants: %d\n\n", consonant);
    printf("Digits: %d\n", digit);
    printf("White spaces: %d", space);

    return 0;
}
```