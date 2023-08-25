---
cssclass:
- t-w
- table-nalt
title: JavaRegex
creation-date: 2023-08-07
aliases:
tags:
- Java
- Java/java.util/regex
---
**[[Java#Java Basics|HOME [Java]]]**

---
# Regular Expression
an [[JavaAPI|API]] to define a pattern for searching or manipulating strings.
> It is widely used to define the constraint on strings such as password and email validation.

The **Regex API** provides 1 interface and 3 classes in `java.util.regex` package. The java.util.regex package provides following classes and interfaces for regular expressions.
1. `MatchResult` interface
2. `Matcher` class
3. `Pattern` class
4. `PatternSyntaxException` class

<br>

**Capturing groups**
Capturing groups are numbered by counting their opening parentheses from the left to the right. In the expression ((A)(B(C))), for example, there are four such groups −
- `((A)(B(C)))`
- `(A)`
- `(B(C))`
- `(C)`

**Regular Expression Patterns**
Brackets are used to find a range of characters:

| Expression                | Description                                              |
| ------------------------- | -------------------------------------------------------- |
| <center>`[abc]`</center>  | Find one character from the options between the brackets |
| <center>`[^abc]`</center> | one character NOT between the brackets                   |
| <center>`[0-9]`</center>  | one character from the range 0 to 9                      |

**Metacharacters**
Metacharacters are characters with a special meaning:

| Metacharacter             | Description                                                                    |
| ------------------------- | ------------------------------------------------------------------------------ |
| <center>\|</center>       | Find a match for any one of the patterns separated by \| as in: cat\|dog\|fish |
| <center>`.`</center>      | one instance of any character                                                  |
| <center>`^`</center>      | match as the beginning of a string as in: `^Hello`                             |
| <center>`$`</center>      | match at the end of the string as in: `World$`                                 |
| <center>`\d`</center>     | digit, `[0-9]`                                                                 |
| <center>`\D`</center>     | (***negation***)                                                               |
| <center>`\s`</center>     | whitespace character, `[\t\n\x0B\f\r]`                                         |
| <center>`\S`</center>     | (***negation***)                                                               |
| <center>`\w`</center>     | word characters, `[a-zA-Z_0-9]`                                                |
| <center>`\W`</center>     | (***negation***)                                                               |
| <center>`\b`</center>     | match at the beginning of a word like this: `\bWORD`, or `WORD\b`              |
| <center>`\B`</center>     | (***negation***)                                                               | 
| <center>`\uxxxx`</center> | Unicode character specified by the hexadecimal number `xxxx`                   |

**Quantifiers**
Quantifiers define quantities:

| Quantifier                | Description                                           |
| ------------------------- | ----------------------------------------------------- |
| <center>`N+`</center>     | `N` occurs once or more times                         |
| <center>`N*`</center>     | `N` occurs zero or more times                         |
| <center>`N?`</center>     | `N` occurs once or not at all                         |
| <center>`N{x}`</center>   | `N` occurs `x` times only                             |
| <center>`N{x,y}`</center> | `N` occurs at least `x` times but less than `y` times | 
| <center>`N{x,}`</center>  | `N` occurs `x` or more times                          |

**Examples:**
- [[JavaRegexExample0|The use of `.` (dot) example]]
- [[JavaRegexExample1|Using the String class]]

<br>

# 
---
- [Java Regex | Regular Expression - javatpoint](https://www.javatpoint.com/java-regex)
- [Pattern (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)
- **CHEATSHEET**: [Regular Expressions Cheat Sheet by DaveChild](https://cheatography.com/davechild/cheat-sheets/regular-expressions/)
- **TOOL**: [RegExr: Learn, Build, & Test RegEx](https://regexr.com/)
- [Top 15 Commonly Used Regex - Digital Fortress](https://digitalfortress.tech/tips/top-15-commonly-used-regex/)