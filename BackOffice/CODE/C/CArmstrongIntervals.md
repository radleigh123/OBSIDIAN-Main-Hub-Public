---
aliases:
---
**tags:** #C/Loop #C/math #C/Miscellaneous/conversion 
**[[1ControlFlow|BACK]]**

---
```C
// Armstrong number... abc = a^n + b^n + c^n
#include <math.h>
#include <stdio.h>

int main() {
   int num, originalNum, remainder, n = 0;
   float result = 0.0;

   printf("Enter an integer: ");
   scanf("%d", &num);

   originalNum = num;

   // store the number of digits of num in n
   for (originalNum = num; originalNum != 0; ++n) {
       originalNum /= 10;
   }

   for (originalNum = num; originalNum != 0; originalNum /= 10) {
       remainder = originalNum % 10;

      // store the sum of the power of individual digits in result
      result += pow(remainder, n);
   }

   // if num is equal to result, the number is an Armstrong number
   if ((int)result == num)
    printf("%d is an Armstrong number.", num);
   else
    printf("%d is not an Armstrong number.", num);
   return 0;
}
```

```C
// Armstrong Numbers between Two intervals
#include <math.h>
#include <stdio.h>
int main() {
  int low, high, number, originalNumber, rem, count = 0;
  double result = 0.0;
  printf("Enter two numbers(intervals): ");
  scanf("%d %d", &low, &high);
  printf("Armstrong numbers between %d and %d are: ", low, high);

  // swap numbers if high < low
  if (high < low) {
    high += low;
    low = high - low;
    high -= low;
  }
   
  // iterate number from (low + 1) to (high - 1)
  // In each iteration, check if number is Armstrong
  for (number = low + 1; number < high; ++number) {
    originalNumber = number;

    // number of digits calculation
    while (originalNumber != 0) {
      originalNumber /= 10;
      ++count;
    }

    originalNumber = number;

    // result contains sum of nth power of individual digits
    while (originalNumber != 0) {
      rem = originalNumber % 10;
      result += pow(rem, count);
      originalNumber /= 10;
    }

    // check if number is equal to the sum of nth power of individual digits
    if ((int)result == number) {
      printf("%d ", number);
    }

    // resetting the values
    count = 0;
    result = 0;
  }

  return 0;
}
```