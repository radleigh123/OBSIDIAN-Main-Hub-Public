---
cssclass: t-w
aliases:
tags:
- C/Operators
- C/Lecture
---
**[[Coperators|BACK]]**

---
## Arithmetic Operator
all are [[COPERATORSbinary|binary operators]], means two operands are required.
![[CARITHMETICsample.svg|center wm-sm cover]]

**Precedence:**

| Operators     | Associativity |
| ------------- | ------------- |
| `*`, `/`, `%` | left to right |
| `+`, `-`      | left to right | 

```C
#include <stdio.h>

int main()
{
    int num1 = 5 + 2 * 3;
    int num2 = (5 + 2) * 3;

    printf("%d %d", num1, num2); // 11 21
    return 0;
}
```