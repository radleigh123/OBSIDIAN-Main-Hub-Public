---
aliases:
---
**tags:** #C/Strings #C/Miscellaneous/macros #C/Miscellaneous/Data_Type 
**[[CCODES|BACK]]**

---
## Additional Topics

### Predefined Macros
- **[date](CMacrodate.md)**
- **[file](CMacrofile.md)**
- **[line](CMacroline.md)**
- **[stdc](CMacrostdc.md)**
- **[time](CMacrotime.md)**

### enum
```C
/* enum - a special kind of data type defined by the user. It consists of constant integrals or integers that are given 
names by a user. */

#include<stdio.h>

enum designFlags{
    BOLD = 1,
    ITALICs = 2,
    UNDERLINE = 4
} button;

int main(){
    int myDesign = BOLD | UNDERLINE;

    //   00000001
    // | 00000100
    // ----------
    //   00000101

    printf("%d", myDesign);

    return 0;
}
```

### `Cmacro`
```C
// Using #define preprocessor directives

#include<stdio.h>
#define PI 3.1415
// macro as a function call
#define circleArea(r) (PI * r * r)

int main(){
    double radius;
    printf("Enter radius: ");
    scanf("%lf", &radius);

    printf("Area = %.2lf", circleArea(radius));

    return 0;
}
```