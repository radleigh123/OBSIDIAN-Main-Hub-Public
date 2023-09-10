---
cssclasses: []
aliases: []
tags:
  - Java
  - Java/ControlFlow
---
**[[Java#Java Basics|HOME [Java]]]**

---
## Printing Patterns
**Pyramid**
```
    * 
   * * 
  * * * 
 * * * * 
* * * * *
```
```java
int n = 5; 
for (int i = 0; i < n; i++) //outer loop for number of rows(n)
{ 
	for (int j=n-i; j > 1; j--) { 
		System.out.print(" ");
	}
	
	for (int j = 0; j <= i; j++ ) { 
		System.out.print("* ");
	} 
	
	System.out.println();
}
```

>[!column|clean no-t flex]
>>[!NOTE|clean no-i] Right Triangle
>> ```
>> *
>> * *
>> * * *
>> * * * *
>> * * * * *
>> ```
>> ```java
>> int n = 5;
>> int i, j;  
>> 
>> for(i = 0; i < n; i++)
>> {
>> 	for(j = 2 * (n - i); j >= 0; j--) {
>> 		System.out.print(" ");
>> 	} 
>> 	for(j = 0; j <= i; j++) {
>> 		System.out.print("* ");
>> 	}
>> 	
>> 	System.out.println();
>> }
>> ```
>
>>[!NOTE|clean no-i] Left Triangle
>> ```
>>         * 
>>       * * 
>> 	* * * 
>>   * * * * 
>> * * * * *
>> ```
>> ```java
>> int n = 5;
>> int i, j;  
>> 
>> for(i = 0; i < n; i++) {
>> 	for(j = 2 * (n-i); j >= 0; j--) {
>> 			System.out.print(" ");
>> 	} 
>> 	
>> 	for(j = 0; j <= i; j++) {
>> 		System.out.print("* ");
>> 	}
>> 	
>> 	System.out.println();
>> } 
>> ```

**Right Pascal's Triangle**
```
*
* *
* * *
* * * *
* * * * *
* * * *
* * *
* *
*
```
```java
int rows = 5;

for (int i = 0; i <= rows-1 ; i++)
{
	for (int j = 0; j <= i; j++) {
	System.out.print("*" + " ");
	}
	
	System.out.println("");
}
	
for (int i = rows - 1; i >= 0; i--)
{
	for(int j = 0; j <= i - 1;j++) {
		System.out.print("*" + " ");
	}

	System.out.println("");
}
```

**Triangle**
```
    *
   * *
  *   *
 *     *
*********
```
```java
int rows = 5;
             
for (int i = 1; i <= rows ; i++)
{
	for (int j = i; j < rows ; j++) {
		System.out.print(" ");
	}
	
	for (int k = 1; k <= (2 * i - 1) ;k++) {
		if( k == 1 || i == rows || k == (2 * i - 1)) {
			System.out.print("*");
		} else {
			System.out.print(" ");
		}
	}
	
	System.out.println("");
}
```

**Diamond**
```
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
```
```java
int rows = 5;    
for (int i=1; i<= rows ; i++)
{ 
	for (int j = rows; j > i ; j--) {
		System.out.print(" ");
	}
	
	System.out.print("*");
	for (int k = 1; k < 2*(i -1) ;k++) {
		System.out.print(" ");
	}
	
	if(i == 1) {
		System.out.println("");
	} else {
		System.out.println("*");
	}
}

for (int i=rows-1; i>= 1 ; i--)
{
	for (int j = rows; j > i ; j--) {
		System.out.print(" ");
	}
	
	System.out.print("*");
	
	for (int k = 1; k < 2*(i -1) ;k++) {
		System.out.print(" ");
	}
	
	if( i==1) {
		System.out.println("");
	} else {
		System.out.println("*");
	}
}
```

<br>

# 
---
- [30 Pattern Programs in Java: Star, Number & Character Patterns](https://www.edureka.co/blog/30-pattern-programs-in-java/)