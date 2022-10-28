---
aliases:
tags:
- CSS/Selectors/Attribute 
---
**[[CSSselectors|BACK]]** | **[[CSS|HOME [CSS]]]**

---
## Attribute Selectors
> The CSS **attribute selector** matches elements based on the presence or value of a given attribute.

### Syntax
**`[attr]`**
Represents elements with an attribute name of _attr_.

**`[attr=value]`**
Represents elements with an attribute name of _attr_ whose value is exactly _value_.

**`[attr~=value]`**
Represents elements with an attribute name of _attr_ whose value is a whitespace-separated list of words, one of which is exactly _value_.

**`[attr|=value]`**
Represents elements with an attribute name of _attr_ whose value can be exactly _value_ or can begin with _value_ immediately followed by a hyphen, `-` (U+002D). It is often used for language subcode matches.

**`[attr^=value]`**
Represents elements with an attribute name of _attr_ whose value is prefixed (preceded) by _value_.

**`[attr$=value]`**
Represents elements with an attribute name of _attr_ whose value is suffixed (followed) by _value_.

**`[attr*=value]`**
Represents elements with an attribute name of _attr_ whose value contains at least one occurrence of _value_ within the string.

**`[attr operator value i]`**
Adding an `i` (or `I`) before the closing bracket causes the value to be compared case-insensitively (for characters within the ASCII range).

**`[attr operator value s]`** *Experimental*
Adding an `s` (or `S`) before the closing bracket causes the value to be compared case-sensitively (for characters within the ASCII range).

>[!EXAMPLE]-
>```CSS
>a {
  color: blue;
}
>
/* Internal links, beginning with "#" */
a[href^="#"] {
  background-color: gold;
}
>
/* Links with "example" anywhere in the URL */
a[href*="example"] {
  background-color: silver;
}
>
/* Links with "insensitive" anywhere in the URL,
   regardless of capitalization */
a[href*="insensitive" i] {
  color: cyan;
}
>
/* Links with "cAsE" anywhere in the URL,
with matching capitalization */
a[href*="cAsE" s] {
  color: pink;
}
>
/* Links that end in ".org" */
a[href$=".org"] {
  color: red;
}
>
/* Links that start with "https" and end in ".org" */
a[href^="https"][href$=".org"] {
  color: green;
}
>```
>
>```HTML
> <ul>
> 	<li><a href="#internal">Internal link</a></li>
> 	<li><a href="http://example.com">Example link</a></li>
> 	<li><a href="#InSensitive">Insensitive internal link</a></li>
> 	<li><a href="http://example.org">Example org link</a></li>
> 	<li><a href="https://example.org">Example https org link</a></li>
> </ul>
>```

# 

<br>

---
**Sources:**
- https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors