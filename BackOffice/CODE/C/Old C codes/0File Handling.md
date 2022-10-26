---
aliases:
---
**tags:** #C/File_Handling 
**[[CCODES|BACK]]**

---
### Binary File
- **[Read Binary](CReadBinary.md)**
- **[Write Binary](CWriteBinary.md)**

### Text File
- **[Read Text](CReadText.md)**
- **[Write Text](CWriteText.md)**

### Seek
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
        printf("Error! can't load file.");
        exit(1);
    }
    
    // Moves the cursor to the end of the file
    fseek(ptr, -sizeof(struct threeNum), SEEK_END);

    for (int i = 0; i < 5; i++){
        fread(&number, sizeof(struct threeNum), 1, ptr);
        printf("n1: %d\tn2: %d\tn3: %d\tn4: %d\n", number.num1, number.num2, number.num3);
        fseek(ptr, -2 * sizeof(struct threeNum), SEEK_CUR);
    }
    fclose(ptr);

    return 0;
}
```