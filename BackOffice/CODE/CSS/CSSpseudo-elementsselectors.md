---
aliases: [pseudo]
tags:
- CSS/Basics/Selectors/Pseudo-elements
- 
---
**[[CSSselectors|BACK]]** | **[[CSS|HOME [HOME]]]**

---
## CSS Pseudo-elements
>[!INFO]- A CSS pseudo-element is used to style specified parts of an element.
>For example, it can be used to:
>- Style the first letter, or line, of an element
>- Insert content before, or after, the content of an element

>[!INFO]- Syntax
>```CSS
> selector: :pseduo-element {
> 	property: value;
> }
>```

### The ::first-line Pseudo-element
- The `::first-line` pseudo-element is used to add a special style to the first line of a text.
```CSS
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
```
>[!NOTE] The ::first-line pseudo-element can only be applied to block-level elements.

The following properties apply to the `::first-line` pseudo-element:
-   font properties
-   color properties
-   background properties
-   word-spacing
-   letter-spacing
-   text-decoration
-   vertical-align
-   text-transform
-   line-height
-   clear

>[!WARNING]- Note:
> **Notice the double colon notation -** `::first-line` versus `:first-line`  
> The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between **pseudo-classes** and **pseudo-elements**.  
> The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1.  
> For backward compatibility, the single-colon syntax is acceptable for CSS2 and CSS1 pseudo-elements.

### The ::first-letter Pseudo-element
- The `::first-letter` pseudo-element is used to add a special style to the first letter of a text.
```CSS
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
```
>[!NOTE] Note:
> The **::first-letter** pseudo-element can only be applied to block-level elements.

# 

<br>

---
**Sources:**
- https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements