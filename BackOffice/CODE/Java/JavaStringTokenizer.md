---
cssclass:
- t-w
- table-nalt
aliases:
tags:
- Java
- Java/StringTokenizer
---
**[[Java#Java Basics|HOME[Java]]]**

---
## StringTokenizer class
The **java.util.StringTokenizer** class allows you to break a String into tokens. It is simple way to break a String. It doesn't provide the facility to differentiate numbers, quoted strings, identifiers etc. like [[JavaStreamTokenizer|StreamTokenizer]] class.
> a legacy class of Java

![[JavaStringTokenizer.png|center]]

| **<center>Methods</center>**     | **<center>Description</center>**                                                             |
| -------------------------------- | ------------------------------------------------------------ |
| `boolean hasMoreTokens()`        | It checks if there is more tokens available.                 |
| `String nextToken()`             | It returns the next token from the StringTokenizer object.   |
| `String nextToken(String delim)` | It returns the next token based on the delimiter.            |
| `boolean hasMoreElements()`      | It is the same as hasMoreTokens() method.                    |
| `Object nextElement()`           | It is the same as nextToken() but its return type is Object. |
| `int countTokens()`              | It returns the total number of tokens.                       |

>[!aside|right]-
> ```
> my
> name
> is
> khan
> ```

```java
import java.util.StringTokenizer;  
public class Simple{  
	public static void main(String args[]){  
		StringTokenizer st = new StringTokenizer("my name is khan"," ");  
		
		 while (st.hasMoreTokens()) {  
			 System.out.println(st.nextToken());  
		 }  
	}  
}  
```

<br>

# 
---
- [StringTokenizer (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/StringTokenizer.html)
- [StringTokenizer in Java - javatpoint](https://www.javatpoint.com/string-tokenizer-in-java)