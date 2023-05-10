---
aliases:
tags:
- C
- 
---
**[[CHackerRank|BACK]]**

---
Given an array, of size , reverse it.
Example: If array, $arr = [1, 2, 3, 4, 5]$, after reversing it, the array should be, $arr = [5, 4, 3, 2, 1]$.

**Input Format**
The first line contains an integer, $n$, denoting the size of the array. The next line contains $n$ space-separated integers denoting the elements of the array.

**Constraints**
$1 \le n \le 1000$
$1 \le arr \le 1000$, where $arr_i$ is the $i^{th}$ element of the array

**Output Format**
The output is handled by the code given in the editor, which would print the array.

**Sample Input 0**
```
6
16 13 7 2 1 12
```

**Sample Output 0**
```
12 1 2 7 13 16
```

**Explanation 0**
Given array, $arr = [16, 13, 7, 2, 1, 12]$. After reversing the array, $arr = [12, 1, 2, 7, 13, 16]$

**Source Code**
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int num, *arr, i;
    scanf("%d", &num);
    arr = (int *)malloc(num * sizeof(int));
    for (i = 0; i < num; i++)
    {
        scanf("%d", arr + i);
    }

    for (int j = 0, k = num - 1; j < num / 2; j++, k--)
    {
        int tmp = *(arr + j);
        *(arr + j) = *(arr + k);
        *(arr + k) = tmp;
    }

    for (i = 0; i < num; i++)
    {
        printf("%d ", *(arr + i));
    }

    free(arr);
    return 0;
}
```