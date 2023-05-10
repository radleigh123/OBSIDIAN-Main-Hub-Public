---
aliases:
tags:
- C
---
**[[CHackerRank|BACK]]**

---
## Printing Pattern Using Loops
Print a pattern of numbers from  to  as shown below. Each of the numbers is separated by a single space.
```
	4 4 4 4 4 4 4  
	4 3 3 3 3 3 4   
	4 3 2 2 2 3 4   
	4 3 2 1 2 3 4   
	4 3 2 2 2 3 4   
	4 3 3 3 3 3 4   
	4 4 4 4 4 4 4 
```

**Input Format**
The input will contain a single integer $n$.

**Constraints**
$1 \le n \le 1000$

**Sample Input 0**
```
2
```

**Sample Output 0**
```
	2 2 2
	2 1 2
	2 2 2
```

**Sample Input 1**
```
5
```

**Sample Output 1**
```
	5 5 5 5 5 5 5 5 5 
	5 4 4 4 4 4 4 4 5 
	5 4 3 3 3 3 3 4 5 
	5 4 3 2 2 2 3 4 5 
	5 4 3 2 1 2 3 4 5 
	5 4 3 2 2 2 3 4 5 
	5 4 3 3 3 3 3 4 5 
	5 4 4 4 4 4 4 4 5 
	5 5 5 5 5 5 5 5 5
```

**Solution:**
```C
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main()
{
    int n;
    scanf("%d", &n);

    int size = n * 2 - 1;

    for (size_t i = 0; i < size; i++)
    {
        for (size_t j = 0; j < size; j++)
        {
            int min = i < j ? i : j;

            min = min < size - i ? min : size - i - 1;
            min = min < size - j - 1 ? min : size - j - 1;

            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```

<br>

# 
---
- [HackerRank - Printing Patter Using Loops in C](https://www.hackerrank.com/challenges/printing-pattern-2/problem?isFullScreen=true&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen)