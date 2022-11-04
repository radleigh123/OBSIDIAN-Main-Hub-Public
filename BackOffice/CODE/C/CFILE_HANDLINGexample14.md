---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/Structures/File_Handling
---
**[[Cfilehandling|BACK]]**

---
>[!recite|alt-co no-i collapse] Reading and Writing [[CSTRUCTURESarraystructure|Array of Structure]] into file
```C
#include <stdio.h>
#include <stdlib.h>

struct book {
    int num;
    char title[10];
};

int main() {
	// Writing in the Bin file
    FILE *fptr;
    if ((fptr = fopen("proto.bin", "wb")) == NULL) {
        printf("Error!");
        exit(1);
    }
    struct book b[5];
    printf("Enter 5 Book details...\n");
    for (int i = 0; i < 5; i++) {
        printf("Enter %d Book no: ", i + 1);
        scanf("%d", &b[i].num);
        while ((getchar()) != '\n'); // flush input buffer
        printf("Enter Book title: ");
        gets(b[i].title);
    }
    fwrite(b, sizeof(struct book), 5, fptr);
    fclose(fptr);

	// Reading the Bin file
    if ((fptr = fopen("proto.bin", "rb")) == NULL) {
        printf("Error!");
        exit(1);
    }
    struct book b[5];
    fread(b, sizeof(struct book), 5, fptr);
    for (int i = 0; i < 5; i++) {
        printf("%d. %s\n", b[i].num, b[i].title);
    }

	fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [Reading and writing array of structure into file using file handling | c programming by sanjay gupta - YouTube](https://www.youtube.com/watch?v=jxTGwfoD4Nc&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=35)