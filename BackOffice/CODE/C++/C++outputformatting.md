---
title: C++outputformatting
creation-date: 2023-01-07
aliases:
tags:
- CPP/Lecture
- CPP/Library/io/Manipulators
- CPP/Library/io/endl
- CPP/Library/io/flush
- CPP/Library/io/setw
- CPP/Library/io/left
- CPP/Library/io/right
- CPP/Library/io/internal
- CPP/Library/io/setfill
- CPP/Library/io/showpos
- CPP/Library/io/boolalpha
- CPP/Library/io/dec
- CPP/Library/io/oct
- CPP/Library/io/hex
- CPP/Library/io/uppercase
- CPP/Library/io/fixed
- CPP/Library/io/scientific
- CPP/Library/io/hexfloat
---
**[[C++|HOME [C++]]]**

---
# Output formatting
**`std::endl`**
outputs '\n' and flushes the output stream

**`std::flush`**
flushes the output stream

**[[C++setw|`std::setw()`]]**
changes the width of the next input/output field

**[[C++left|`std::left`]]**, **[[C++left|`std::right`]]**, **[[C++left|`std::internal`]]**
sets the placement of fill characters

**[[C++setfill|`std::setfill()`]]**
changes the fill character

**[[C++showpos|`std::showpos`]]**, **[[C++showpos|`std::noshowpos`]]**
controls whether the `+` sign used with non-negative numbers

**[[C++boolalpha|`std::boolalpha`]]**, **[[C++boolalpha|`std::noboolalpha`]]**
switches between textual and numeric representation of booleans

**[[C++dechexoct|`std::dec`]]**, **[[C++dechexoct|`std::hex`]]**, **[[C++dechexoct|`std::oct`]]**
changes the base used for integer I/O

**[[C++showbase|`std::showbase`]]**, **[[C++showbase|`std::noshowbase`]]**
controls whether prefix is used to indicate numeric base

**[[C++uppercase|`std::uppercase`]]**, **[[C++uppercase|`std::nouppercase`]]**
controls whether uppercase characters are used with some output formats

**[[C++fixedscientifichex|`std::fixed`]]**, **[[C++fixedscientifichex|`std::scientific`]]**, **[[C++fixedscientifichex|`std::hexfloat`]]**, **[[C++fixedscientifichex|`std::defaultfloat`]]**
changes formatting used for floating-point I/O
>[!TIP|alt-co] **changing back to default**
> ```cpp
> std::cout.unsetf(std::ios::scientific | std::ios::fixed);
> ```

**[[C++setprecision|`std::setprecision`]]**
changes floating-point precision

**[[C++showpoint|`std::showpoint`]]**, **[[C++showpoint|`std::noshowpoint`]]**
controls whether decimal point is always included in floating-point representation

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/io/manip