---
cssclass: t-c
aliases:
tags:
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Format Specifier
is a string used in the formatted input and output functions.

|              | Meaning                                                                                                                                                                   |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `%d` or `%i` | print the signed integer value where signed integer means that the variable can hold both positive and negative values                                                    |
| `%u`         | print the unsigned integer value where the unsigned integer means that the variable can hold only positive value                                                          |
| `%o`         | print the octal unsigned integer where octal integer value always starts with a 0                                                                                         |
| `%x`         | print the hexadecimal unsigned integer where the hexadecimal integer value always starts with a 0x value                                                                  |
| `%X`         | print the hexadecimal unsigned integer, but %X prints the alphabetical characters in uppercase such as A, B, C, etc                                                       |
| `%f`         | printing the decimal floating-point values                                                                                                                                |
| `%e` or `%E` | used for scientific notation. It is also known as Mantissa or Exponent                                                                                                    |
| `%g`         | print the decimal floating-point values, and it uses the fixed precision, i.e., the value after the decimal in input would be exactly the same as the value in the output |
| `%p`         | print the address in a hexadecimal form.                                                                                                                                  |
| `%c`         | print the unsigned character                                                                                                                                              |
| `%s`         | print the strings                                                                                                                                                         |
| `%ld`        | print the long-signed integer value                                                                                                                                       |

<br>

# 
---
**Sources:**
- [C Format Specifier - javatpoint](https://www.javatpoint.com/c-format-specifier)