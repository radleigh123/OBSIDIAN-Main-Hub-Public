---
aliases:
tags:
- Java
- Java/Lecture
- Java/ControlFlow/break
- Java/ControlFlow/continue
- Java/ControlFlow/return
---
**[[JavaFlowControl|BACK]]**

---
## The Branching Statement
**break**
>[!column|flex no-t] has two forms:
>>[!INFO|clean no-i] ***labeled form***
>> (terminates an outer statement labeled "foo")
>> ```java
>> search:
>> 	for (i = 0; i < arrayOfInts.length; i++) {
>> 		for (j = 0; j < arrayOfInts[i].length; j++) {
>> 			if (arrayOfInts[i][j] == searchfor) {
>> 				foundIt = true;
>> 				break search; // `search` keyword
>> 			}
>> 		}
>> 	}
>> ```
>
>>[!INFO|clean no-i] ***unlabeled form***
>> (in the switch statements, also use to terminate loops)
>> ```java
>> for (i = 0; i < arrayOfInts.length; i++) {
>> 	if (arrayOfInts[i] == searchfor) {
>> 	foundIt = true;
>> 	break;
>> 	}
>> }
>> ```

**continue**
>[!column|flex no-t] has two forms:
>>[!INFO|clean no-i] ***labeled form***
>> (terminates an outer statement labeled "foo")
>> ```java
>> search:
>> 	for (i = 0; i < arrayOfInts.length; i++) {
>> 		for (j = 0; j < arrayOfInts[i].length; j++) {
>> 			if (arrayOfInts[i][j] == searchfor) {
>> 				foundIt = true;
>> 				continue search; // `search` keyword
>> 			}
>> 		}
>> 	}
>> ```
>
>>[!INFO|clean no-i] ***unlabeled form***
>> (in the switch statements, also use to terminate loops)
>> ```java
>> for (i = 0; i < arrayOfInts.length; i++) {
>> 	if (arrayOfInts[i] == searchfor) {
>> 	foundIt = true;
>> 	continue;
>> 	}
>> }
>> ```

**return**
statement exits from the current method, and control flow returns to where the method was invoked
```java
return; // used when method is void, no return value
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/branch.html