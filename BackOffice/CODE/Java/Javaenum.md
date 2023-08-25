---
cssclass:
title: Javaenum
creation-date: 2023-08-08
aliases:
tags:
- Java
- Java/enum
---
**[[Java#Java Basics|HOME[Java]]]**

---
# Enumerated type: `enum`
`enum` is a special "class" that represents a group of **constants** (unchangeable variables, like `final` variables)
> different from `Enumeration` interface (legacy), now superseded by [[JavaIterator&Enumeration|Iterator]]

```java
enum Level {
	LOW {
		@Ovveride
		public String toString() {
			return "This is " + Level.LOW.name();
		}
	},
	MEDIUM,
	HIGH
}

Level.ordinal(LOW) // 0
Level.LOW.compareTo(Level.MEDIUM) // Level.ordinal(LOW) - Level.ordinal(MEDIUM)

LOW.toString() // This is LOW
Level.LOW.name() // LOW

Level.valueOf("LOW") // LOW
Level.values() // Level[]
```

>[!TIP]- Why And When To Use **enums**?
> Use enums when you have values that you know aren't going to change, like month days, days, colors, deck of cards, etc.

**EnumSet**
is a specialized [[JavaSet|Set]] implementation that's meant to be used with `Enum` types. The _**EnumSet**_ is an abstract class that has two implementations, `RegularEnumSet` and `JumboEnumSet`, one of which is chosen depending on the number of constants in the `enum` at the time of instantiation.
```java
EnumSet<Level> levelStatus = EnumSet.of(Level.LOW, Level.MEDIUM, Level.HIGH);
```

<br>

**EnumMap**
is a specialized Map implementation meant to be used with enum constants as keys. Compared to its counterpart [[JavaHashtableHashMap|HashMap]], it's an efficient and compact implementation that's internally represented as an array.
```java
EnumMap<Level, List<AnyClass>> levelStatus(List<Level> levels) = new EnumMap<>(Level.class);
```

<br>

**Examples:**
- [[JavaenumExample0|Object references in enums]]

<br>

# 
---
- [Enum Types (The Java™ Tutorials) (oracle.com)](https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html)
- [A Guide to Java Enums | Baeldung](https://www.baeldung.com/a-guide-to-java-enums)
- [Java Enums (w3schools.com)](https://www.w3schools.com/java/java_enums.asp)