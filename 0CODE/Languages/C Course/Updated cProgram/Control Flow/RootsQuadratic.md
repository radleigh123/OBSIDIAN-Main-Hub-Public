```C
// Program to find Roots of a Quadratic Equation
#include<stdio.h>
#include<math.h>
int main(){
    double a, b, c, discriminant, root1, root2, realPart, imagPart;
    printf("Enter coefficients (a,b,c): ");
    scanf("%lf", &a, &b, &c);

    discriminant = b * b - 4 * a * c;
    printf("%.2lf\n", discriminant);

    // condition for real and different roots
    if (discriminant > 0){
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        printf("root1 = %.2lf and root2 = %.2lf", root1, root2);
    }
    
    // condition for real and equal roots
    else if (discriminant == 0){
        root1 = root2 = -b / (2 * a);
        printf("root1 = root2 = %.2lf", root1);
    }

    // if roots are not real
    else
    {
        realPart = -b / (2 * a);
        imagPart = sqrt(-discriminant) / (2 * a);
        printf("root1 = %.2lf+%.2lfi and root2 = %2.lf-%2.lfi", realPart, imagPart, realPart, imagPart);
    }

    return 0;
}
```