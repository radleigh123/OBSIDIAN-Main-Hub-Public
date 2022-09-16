#C #CFileHandling 

```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int num;
    FILE *fptr;

    fptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\C Learn\\File Handling\\Write.txt", "w");

    if (fptr == NULL){
        printf("Error!");
        exit(1);
    }
    
    printf("Enter num: ");
    scanf("%d", &num);

    // a function is used to write set of characters into file. 
    // It sends formatted output to a stream.
    fprintf(fptr, "%d", num);

    fclose(fptr);

    return 0;
}
```