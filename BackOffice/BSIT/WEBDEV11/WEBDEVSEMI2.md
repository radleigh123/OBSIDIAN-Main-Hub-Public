---
title: Margins and Padding
creation-date: 2022-10-26
aliases:
tags:
---
**[[WEBDEV11LEC#^SEMICH2|BACK]]**

---
## Margins
- The **`margin`** property defines the spaces around an [[WEBDEVelements|HTML element]] outside its border.
- CSS properties than can be used to define the margin on each side of an element such as:
	- *margin-top*
	- *margin-right*
	- *margin-bottom*
	- *margin-left*
	- *margin*.

## Padding
- The **`padding`** property defines the space between the content of an HTML element and its border
- CSS properties that can be used to define the padding for each side of an element such as
	- *padding-top*
	- *padding-right*
	- *padding-bottom*
	- *padding-left*
	- *padding*

```HTML CSS
<!DOCTYPE html>
<html>
    <head>
        <style>
            .myStyle {
                border: 10px groove red;
                margin-top: 45px;
                margin-left: 60px;
                padding-left: 50px;
                padding-top: 30px;
                padding-bottom: 80px;
            }
        </style>
    </head>
    <body>
        <p>This is how CSS margin and padding properties work.</p>
        <p class = "myStyle">This is how CSS margin and padding properties work.</p>
    </body>
</html>
```