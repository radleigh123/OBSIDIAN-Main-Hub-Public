---
cssclass:
aliases:
tags:
- Java
- 
---
**[[JavaRegex|BACK]]**

---
>[!aside|right]-
> ```
> 011234567
> Correct format.
> ```

```java
System.out.print("Provide a student number: ");
String number = scanner.nextLine();

if (number.matches("01[0-9]{7}")) {
	// CORRECT FORMAT 011234567
	System.out.println("Correct format.");
} else {
	// INCORRECT FORMAT 01123
	System.out.println("Incorrect format.");
}
```