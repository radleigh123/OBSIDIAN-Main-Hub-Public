---
aliases:
tags:
- C
- 
---
**[[CHackerRank|BACK]]**

---
**Objective**

In this challenge, you will learn the usage of the _for_ loop, which is a programming language statement which allows code to be executed until a terminal condition is met. They can even repeat forever if the terminal condition is never met.

The syntax for the `for` loop is:
```
for ( <expression_1> ; <expression_2> ; <expression_3> )
	<statement>
```
-   _expression_1_ is used for intializing variables which are generally used for controlling the terminating flag for the loop.
-   _expression_2_ is used to check for the terminating condition. If this evaluates to false, then the loop is terminated.
-   _expression_3_ is generally used to update the flags/variables.

The following loop initializes  to 0, tests that  is less than 10, and increments  at every iteration. It will execute 10 times.
```
for(int i = 0; i < 10; i++) {
    ...
}
```

**Task**
For each integer $n$ in the interval $|a, b|$ (given as input) :
-   If $1 \le n \le 9$, then print the English representation of it in lowercase. That is "one" for $1$, "two" for $2$, and so on.
-   Else if $n \ge 9$ and it is an even number, then print "even".
-   Else if $n \ge 9$ and it is an odd number, then print "odd".

**Input Format**
The first line contains an integer, $a$.
The second line contains an integer, $b$.

**Constraints**
$1 \le a \le b \le 10^6$

**Output Format**
Print the appropriate English representation,`even`, or `odd`, based on the conditions described in the 'task' section.
**Note:** $|a,b| = \{x \in \mathbb{Z}\ |\ a \le x \le b\} = \{a, a + 1, ..., b\}$

**Sample Input**
```
8
11
```

**Sample Output**
```
eight
nine
even
odd
```

**Source Code**
```C
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main()
{
    int a, b;
    scanf("%d\n%d", &a, &b);

    if (a < 1 || a > b || b > pow(10, 6))
    {
        return 0;
    }

    for (int i = a; i <= b; i++)
    {
        switch (i)
        {
        case 1:
            printf("one");
            break;
        case 2:
            printf("two");
            break;
        case 3:
            printf("three");
            break;
        case 4:
            printf("four");
            break;
        case 5:
            printf("five");
            break;
        case 6:
            printf("six");
            break;
        case 7:
            printf("seven");
            break;
        case 8:
            printf("eight");
            break;
        case 9:
            printf("nine");
            break;
        default:
            if (i % 2 == 0)
            {
                printf("even");
            }
            else
            {
                printf("odd");
            }
            break;
        }
        printf("\n");
    }

    return 0;
}
```