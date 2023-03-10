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
> *Bound mismatch: The type Character is not a valid substitute for the bounded parameter <TENTEN extends Number> of the type myGeneric<TENTEN,TENTEN2>*

```java
public class Proto {
    public static void main(String[] args) {

        myGeneric<Integer, Integer> myInt = new myGeneric<>(1, 9);
        myGeneric<Double, Double> myDub = new myGeneric<>(4.5, 6.54);
        myGeneric<Character, Character> myChar = new myGeneric<>('A', 'Ñ'); // ERROR! not a subclass of Number class
        myGeneric<String, Character> myStr = new myGeneric<>("Rhiz Caballero", 'O'); // ERROR! not a subclass of Number class

        System.out.println(myInt.getValue());
        System.out.println(myDub.getValue());
        System.out.println(myChar.getValue());
        System.out.println(myStr.getValue());

    }
}
```
```java
public class myGeneric<TENTEN extends Number, TENTEN2 extends Number> {

    TENTEN x;
    TENTEN2 y;

    myGeneric(TENTEN x, TENTEN2 y) {
        this.x = x;
        this.y = y;
    }

    public TENTEN2 getValue() { return y; }

}
```