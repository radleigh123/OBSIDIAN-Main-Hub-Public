**[[CSS]]**

#CSS #CSSlec 
# How to Add CSS
> When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet.

## Three Ways to insert CSS
- **[External CSS](CSSexternal.md)**
- **[Internal CSS](CSSinternal.md)**
- **[Inline CSS](CSSinline.md)**

## Cascading Order
What style will be used when there is more than one style specified for an HTML element?

All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:
1. inline style (inside an HTML element)
2. External and Internal style sheets (in the head section)
3. Browser default

So, an inline style has the highest priority, and will override external and internal styles and browser defaults.![[Pasted image 20221018031340.png]]

<br>

---
**Sources:**
- [How to add CSS (w3schools.com)](https://www.w3schools.com/css/css_howto.asp)