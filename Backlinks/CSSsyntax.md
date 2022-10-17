**[[CSS]]**

#CSS #CSSlec 
# CSS Syntax
a CSS rules consists of a selector and a [declaration block](CSSdeclarationblock.md).
> [!INFO] **Syntax**
> ![[Pasted image 20221018000651.png]]
>
>- The selector points to the HTML element you want to style.
>- The declaration block contains one or more declarations separated by semicolons.
>- Each declaration includes a CSS property name and a value, separated by a colon.
>	- Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

```CSS
p {
	color: red;
	text-align: center;
}
```
Example explained
- **p** is a selector in CSS (it points to the HTML element you want to style: `<p>`).
- **color** is a property, and <u>red</u> is the property value
- **text-align** is a property, and <u>center</u> is the property value

>[!TIP]- [CSS Declaration Block](CSSdeclarationblock.md)