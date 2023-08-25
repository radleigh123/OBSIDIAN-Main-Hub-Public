---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Introduction|HOME [Java]]]**

---
## Terminologies
- **Expression** - is any word or group of words or symbols that is a value. In programming, an expression is a value, or anything that executes and ends up being a value. For example:
```js
int price = 500;
```
Judging from the code above, <u>`const`</u>, <u>`price`</u>, <u>`=`</u>, and <u>`500`</u> are **expressions** because each of them has a definite and unique meaning or value. But if we take all of them together `const price = 500` - then we have a **statement**.

<br>

-  **Statement**- is a group of expressions and/or statements that you design to carry out a task or an action.
```java
// Inline statement
double price = 150.75;
```
```java
// Block statement
if (true) {
	System.out.println();
}
```
```java
// Loop statement
do {
	int num = 1;
} while(true);
```

>[!EXAMPLE]- Differences between expressions & statements
>- <u>Expressions</u> can be assigned or used as operands, while <u>statements</u> can only be declared.
>- <u>Statements</u> create side effects to be useful, while <u>expressions</u> are values or execute to values.
>- <u>Expressions</u> are unique in meaning, while <u>statements</u> are two-sided in execution. 
>	- e.g, `1` has a certain value while `go( )` may be executed or not.
>- <u>Statements</u> are the whole structure, while <u>expressions</u> are the building blocks. 
>	- e.g., a line or a block of code is a statement.

<br>



<br>

# 
---
- [Statement vs Expression – What's the Difference in Programming? (freecodecamp.org)](https://www.freecodecamp.org/news/statement-vs-expression-whats-the-difference-in-programming/#:~:text=The%20Main%20Differences%20Between%20an,values%20or%20execute%20to%20values.)