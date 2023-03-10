---
cssclass:
aliases:
tags:
- Java
- Java/Generics
- Java/WrapperClass
---
**[[JavaGenerics|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> 1
> 4.5
> A
> Rhiz Caballero

```java
public class Proto {
    public static void main(String[] args) {

        myGeneric<Integer> myInt = new myGeneric<>(1);
        myGeneric<Double> myDub = new myGeneric<>(4.5);
        myGeneric<Character> myChar = new myGeneric<>('A');
        myGeneric<String> myStr = new myGeneric<>("Rhiz Caballero");

        System.out.println(myInt.getValue());
        System.out.println(myDub.getValue());
        System.out.println(myChar.getValue());
        System.out.println(myStr.getValue());

    }
}
```
```java
public class myGeneric<TENTEN> {

    TENTEN x;

    myGeneric(TENTEN x) {
        this.x = x;
    }

    public TENTEN getValue() { return x; }

}
```