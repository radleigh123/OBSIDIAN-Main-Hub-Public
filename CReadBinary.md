#C #CFileHandling

```C
#include<stdio.h>
#include<stdlib.h>

struct threeNum{
    int num1, num2, num3;
};

int main(){
    struct threeNum number;
    FILE *ptr;

    if ((ptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\C Learn\\File Handling\\Binary File\\Program.bin", "rb")) == NULL){
        printf("Error! can't open file.");
        exit(1);
    }
    
    for (int i = 1; i <= 5; i++){
        fread(&number, sizeof(struct threeNum), 1, ptr);
        printf("Number1: %d\tNumber2: %d\tNumber3: %d\n", number.num1, number.num2, number.num3);
    }
    fclose(ptr);

    return 0;
}
```