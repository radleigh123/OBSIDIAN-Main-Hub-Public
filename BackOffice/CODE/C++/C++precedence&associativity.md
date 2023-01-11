---
title: C++precedence&associativity
creation-date: 2023-01-07
aliases:
tags:
- CPP/Lecture
- CPP/Operators
---
**[[C++|HOME [C++]]]**

---
# Precedence & Associativity
**Precedence** - which operation to do first
**Associativity** - which direction/order

![[Pasted image 20230107174816.png|center]]
1. The operand of sizeof can't be a C-style type cast: the expression `sizeof (int) * p` is unambiguously interpreted as `(sizeof(int)) * p`, but not `sizeof((int)*p)`.
2. The expression in the middle of the conditional operator (between `?` and :) is parsed as if parenthesized: its precedence relative to `?`: is ignored.

<br>

>[!INFO|collapse]+ &nbsp&nbsp See also
> ![[Pasted image 20230107174900.png|center]]

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/operator_precedence