---
aliases:
tags:
- Java
- Java/ControlFlow/ifelse
---
**[[JavaFlowControl|BACK]]**

---
## The if-then and if-then-else Statements
**if-then**
```java
void applyBrakes() {
    // the "if" clause: bicycle must be moving
    if (isMoving){ 
        // the "then" clause: decrease current speed
        currentSpeed--;
    }
}
```

**if-then-else**
```java
void applyBrakes() {
    if (isMoving) {
        currentSpeed--;
    } else {
        System.err.println("The bicycle has already stopped!");
    } 
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html