**[[CSS]]**

#CSS #CSSlec 
# CSS Declaration Block
- A CSS declaration block is an ordered collection of CSS properties and values. It is represented in the DOM as a CSSStyleDeclaration.
- Each property and value pairing is known as a CSS declaration. The CSS declaration block has the following associated properties:

>[!EXAMPLE] computed flag
>Set if the CSSStyleDeclaration object is a computed rather than specified style. Unset by default.

>[!EXAMPLE] declarations
>The CSS declarations associated with this object.

>[!EXAMPLE] parent CSS rule
>The CSSRule that the CSS declaration block is associated with, otherwise null.

>[!EXAMPLE] owner node
>The element that the CSS declaration block is associated with, otherwise null.

>[!EXAMPLE] updating flag
>Set when the CSS declaration block is updating the owner node's style attribute.

When a CSSStyleDeclaration is returned by a CSS Object Model (CSSOM) interface these properties are set to appropriate values as defined by the specification.

## Basic example
The following example shows a CSS rule with a declaration block for the `<h1>` element. The CSS declaration block is the lines between the curly braces.
```CSS
h1 {
  margin: 0 auto;
  font-family: "Helvetica Neue", "Arial", sans-serif;
  font-style: italic;
  color: rebeccapurple;
}

```

# 
---
**Sources:**
- [CSS Declaration Block - Web APIs | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model/CSS_Declaration_Block)