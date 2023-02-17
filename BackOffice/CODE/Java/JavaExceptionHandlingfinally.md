---
aliases:
tags:
- Java
- Java/Exceptions/finally
---
**[[JavaExceptionHandling|BACK]]**

---
## `finally` block
is used to execute the necessary code of the program. It is executed whether an exception is handled or not.

**e.g.**
```java
Scanner sc = new Scanner(System.in);

try {
	System.out.print("Input two numbers: ");
	int z = sc.nextInt() / sc.nextInt();

	System.out.println("result: " + z);
} catch (ArithmeticException e) {
	System.out.println("Value can't divide zero");
} finally {
	System.out.println("This will always print");

	sc.close(); // Good thing for closing
}
```