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
> 9
> 6.54
> Ñ
> O

```java
public class Proto {
    public static void main(String[] args) {

        myGeneric<Integer, Integer> myInt = new myGeneric<>(1, 9);
        myGeneric<Double, Double> myDub = new myGeneric<>(4.5, 6.54);
        myGeneric<Character, Character> myChar = new myGeneric<>('A', 'Ñ');
        myGeneric<String, Character> myStr = new myGeneric<>("Rhiz Caballero", 'O');

        System.out.println(myInt.getValue());
        System.out.println(myDub.getValue());
        System.out.println(myChar.getValue());
        System.out.println(myStr.getValue());

    }
}
```
```java
public class myGeneric<TENTEN, TENTEN2> {

    TENTEN x;
    TENTEN2 y;

    myGeneric(TENTEN x, TENTEN2 y) {
        this.x = x;
        this.y = y;
    }

    public TENTEN2 getValue() { return y; }

}
```