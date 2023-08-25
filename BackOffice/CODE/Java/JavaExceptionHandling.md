---
aliases:
tags:
- Java
- Java/Exceptions
---
**[[Java#Error Handling|HOME [Java]]]**

---
## Exception Handling
<mark class="hltr-lightgreen">powerful mechanism to handle the runtime errors</mark> so that the normal flow of the application can be maintained.
> Java forces a programmer to include the error-handling code (e.g. `try`/`catch`, `throws`) for the majority of errors; otherwise the programs won’t even compile.

>[!column|flex clean no-t]
>>[!INFO|clean no-i]+ Types of Exception
>>- **$\mathbf{Checked\ exception}$**
>> \-$\;$The classes that directly inherit the Throwable class except RuntimeException and Error are known as checked exceptions. For example, IOException, SQLException, etc. Checked exceptions are checked at compile-time.
>> 
>>- **$\mathbf{Unchecked\ exception}$**
>> \-$\;$The classes that inherit the RuntimeException are known as unchecked exceptions. For example, ArithmeticException, NullPointerException, ArrayIndexOutOfBoundsException, etc. Unchecked exceptions are not checked at compile-time, but they are checked at runtime.
>> 
>>- **$\mathbf{Error}$**
>> \-$\;$Error is irrecoverable. Some example of errors are OutOfMemoryError, VirtualMachineError, AssertionError etc.
>
>>[!INFO|clean no-i] Keywords
>>- **[[JavaExceptionHandlingtrycatch|try]]** / **[[JavaExceptionHandlingtrycatch|catch]]**
>>- **[[JavaExceptionHandlingfinally|finally]]**
>>- **[[JavaExceptionHandlingthrow|throw]]**
>>- **[[JavaExceptionHandlingthrows|throws]]**

^4a4a2d

<br>

# 
---
- https://www.w3schools.com/java/java_try_catch.asp
- https://www.javatpoint.com/exception-handling-in-java