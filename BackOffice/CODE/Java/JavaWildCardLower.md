---
cssclass:
aliases:
tags:
- Java
- Java/Wildcards/LowerBounded
---
**[[JavaWildCard|BACK]]**

---
## Lower Bounded Wildcard
It is expressed using the _super_ keyword and it specifies the lower class in the hierarchy that can be used as a generic type.

Example:
Suppose we want to write a [[JavaGenericsTypesMethod|generic method]] that adds numbers to a list. Say we don't want to support decimal numbers but only `Integer`. To maximize flexibility, we want to allow users to call our method using the list of `Integer` and all of its *supertypes* (`Number` or `Object`). In other words, anything that can hold `Integer` values. We should use a *lower-bounded wildcard*:
```java
// Here, any subtype can be added into the collection defined with supertype
public static void addNumber(List<? super Integer> list, Integer number) {
    list.add(number);
}
```

> If we are unsure whether we should use the upper or lower bound, we can think about the [[JavaGenericsQuestion|PECS]] (Producer Extends, Consumer Super).

Whenever our method consumes a collection, for example adding elements, we should use a lower bound. On the other hand, if our method only reads elements, we should use the [[JavaWildCardUpper|upper bound]]. Additionally, if our method does both, i.e., it produces and consumes a collection, we can't apply the *PECS rule* and should use [[JavaWildCardUnbounded|unbounded]] types instead.

To clarify, let’s apply the PECS rule to our example. Our generic method modifies the list by adding elements to it. From the list perspective, it allows adding elements but it isn’t safe to read elements. We would get a compiler error if we try to replace the lower bound with an upper bound.

>[!WARNING|alt-co] This type of bound can be used only with a wildcard since type parameters don’t support them.

>[!aside|right show-title]+ RESULT:
> \[4, 5, 6, 7]
> \[4, 5, 6, 7]

```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // The method print will only take Integer or its superclass Number
        List<Integer> list1 = Arrays.asList(4, 5, 6, 7);
        // Integer list object is being passed
        print(list1);

        List<Double> list2 = Arrays.asList(4.1, 5.1, 6.2, 7.2); // COMPILER ERROR!
        print(list2);
    }

    public static void print(List<? super Integer> list) {
        System.out.println(list);
    }
}
```

>[!NOTE|alt-co ttl-c collapse]
> *Use [[JavaWildCardUpper|extend wildcard]] when you want to get values out of a structure and <u>super wildcard</u> when you put values in a structure. Don’t use wildcard when you get and put values in a structure. You can specify an upper bound for a wildcard, or you can specify a lower bound, but you cannot specify both.*

<br>

# 
---
- [wildcard bounds (Baeldung)](https://www.baeldung.com/java-generics-type-parameter-vs-wildcard#bounds)