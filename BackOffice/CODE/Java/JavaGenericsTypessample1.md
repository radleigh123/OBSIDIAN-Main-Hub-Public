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
> 150 true

```java
class Test<T, U> {
    T obj1;
    U obj2;

    Test(T obj1, U obj2) {
        this.obj1 = obj1;
        this.obj2 = obj2;
    }

    public void print() {
        System.out.println(obj1 + " " + obj2);
    }
}

public class Main {
    public static void main(String[] args) {
        Test<Integer, Boolean> obj = new Test<>(150, true);

        obj.print();
    }
}
```