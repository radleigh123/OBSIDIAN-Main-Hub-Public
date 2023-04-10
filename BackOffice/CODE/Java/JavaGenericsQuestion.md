**Q13. When Would You Choose to Use a Lower Bounded Type vs. an Upper Bounded Type?**
When dealing with [[UpdateJava#Collections|collections]], a common rule for selecting between upper or lower bounded wildcards is PECS (**producer extends, consumer super**).This can be easily demonstrated through the use of some standard Java interfaces and classes. 

$\quad$__Producer extends__ just means that if you are creating a producer of a generic type, then use the _extends_ keyword. Let's try applying this principle to a collection, to see why it makes sense:
```java
public static void makeLotsOfNoise(List<? extends Animal> animals) {
    animals.forEach(Animal::makeNoise);   
}
```
Here, we want to call _makeNoise()_ on each animal in our collection. This means our collection is a producer_,_ as all we are doing with it is getting it to return animals for us to perform our operation on. If we got rid of _extends_, we wouldn't be able to pass in lists of cats_,_ dogs or any other subclasses of animals. By applying the producer extends principle, we have the most flexibility possible.

$\quad$__Consumer super__ means the opposite to _producer extends._ All it means is that if we are dealing with something which consumes elements, then we should use the _super_ keyword. We can demonstrate this by repeating our previous example:
```java
public static void addCats(List<? super Animal> animals) {
    animals.add(new Cat());   
}
```
We are only adding to our list of animals, so our list of animals is a consumer. This is why we use the _super_ keyword. It means that we could pass in a list of any superclass of animal, but not a subclass. For example, if we tried passing in a list of dogs or cats then the code would not compile.

<br>

The final thing to consider is what to do if a collection is both a consumer and a producer. An example of this might be a collection where elements are both added and removed. In this case, an unbounded wildcard should be used.

<br>

# 
---
- [Java Generics Interview (Baeldung)](https://www.baeldung.com/java-generics-interview-questions#q13-when-would-you-choose-to-use-a-lower-bounded-type-vs-an-upper-bounded-type)