---
cssclass: t-c, tbl-nalt, t-w, no-m
aliases:
tags:
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Keywords
A keyword is a <mark class="hltr-purple">reserved word</mark>. You cannot use it as a variable name, constant name, etc. There are only 32 reserved words (keywords) in the C language.

|         |          |          |        |          |          |         |     |
| ------- | -------- | -------- | ------ | -------- | -------- | ------- | --- |
| auto    | break    | case     | char   | const    | continue | default | do  |
| double  | else     | enum     | extern |          |          |         |     |
| float   | for      | goto     | if     | int      |          |         |     |
| long    | register | return   |        |          |          |         |     |
| short   | signed   | sizeof   | static | struct   | switch   |         |     |
| typedef | union    | unsigned | void   | volatile | while    |         |     |

---
## Identifiers
C identifiers represent the name in the C program, for example, variables, functions, arrays, structures, unions, labels, etc.
> can be composed of letters such as <mark class="hltr-blue">uppercase</mark>, <mark class="hltr-blue">lowercase letters</mark>, <mark class="hltr-blue">underscore</mark>, <mark class="hltr-blue">digits</mark>, but the starting letter should be either an alphabet or an underscore.

>[!ABSTRACT|alt-co]- Rules of constructing C identifiers
>- The first character of an identifier should be either an alphabet or an underscore, and then it can be followed by any of the character, digit, or underscore.
>- It should not begin with any numerical digit.
>- In identifiers, both uppercase and lowercase letters are distinct. Therefore, we can say that identifiers are case sensitive.
>- Commas or blank spaces cannot be specified within an identifier.
>- Keywords cannot be represented as an identifier.
>- The length of the identifiers should not be more than 31 characters.
>- Identifiers should be written in such a way that it is meaningful, short, and easy to read.

>[!column|flex no-t]
>>[!NOTE|clean no-i] Valid identifiers
>>- `total`
>>- `sum`
>>- `average`
>>- `_m_`
>>- `sum_1`
> 
>>[!NOTE|clean no-i] Invalid identifiers
>>- `2sum` (started w/ numerical digit)
>>- `int` (reserved word)
>>- `char` (reserved word)
>>- `m+n` (special character, '+')