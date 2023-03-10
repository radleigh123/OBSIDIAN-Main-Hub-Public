---
cssclass:
title: LuauTypes
creation-date: 2023-03-09
aliases:
tags:
- Luau
- 
---
**[[Luau|HOME [Luau]]]**

---
# Data Types
- [[Luaunil|nil]] represents non-existence or nothingness. It's different from any other value or data type.
- [[LuauBooleans|Booleans]], or bool, have a value of either false or true.
- [[LuauNumbers|Numbers]], or double, represents double-precision (64-bit) floating-point numbers.
- [[LuauStrings|Strings]] are sequences of characters, such as letters, numbers, and symbols.
- [[LuauTables|Tables]] are arrays or dictionaries of any value except nil.
- [[LuauEnums|Enums]] are fixed lists of items.

Luau is dynamically typed by default. Variables, function parameters, and return values can be any data type. This helps you write code faster because you don't need to provide types for each piece of data. You can still declare explicit types for variables in Luau and enable [[LuauTypeChecking|strict type checking]] to make type issues obvious and easy to locate.