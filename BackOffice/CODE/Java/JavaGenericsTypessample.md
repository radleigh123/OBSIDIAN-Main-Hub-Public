---
cssclass:
aliases:
tags:
- Java
- 
---
**[[JavaGenericsTypes|BACK]]**

---
>[!aside|right show-title]+ RESULT:
> Integer instance: 15
> String instance: Hello World

```java
class mainClass<T> {
    T obj;

    mainClass(T obj) {
        this.obj = obj;
    }

    public T getObject() {
        return this.obj;
    }
}

public class Main {
    public static void main(String[] args) {
        // instance of Integer Type
        mainClass<Integer> iObj = new mainClass<>(15);
        System.out.println("Integer instance: " + iObj.getObject());

        // instance of String Type
        mainClass<String> sObj = new mainClass<>("Hello World");
        System.out.println("String instance: " + sObj.getObject());
    }
}
```