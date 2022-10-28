---
title: Selectors
creation-date: 2022-10-26
aliases:
tags:
- CSS/Selectors/id
- CSS/Selectors/class
- CSS/Selectors/universal
- CSS/Selectors/grouping
---
**[[CSS|HOME [CSS]]]**

---
# Selectors
- selects the HTML [element(s)](CSSelements) you want to style.
>[!INFO] 
>CSS selectors are used to "find" (or select) the HTML elements you want to style.
>We can divide CSS selectors into 5 categories:
>- Simple selectors
>- [Combinator selectors](CSScombinatorselectors.md)
>- [Pseudo-class selectors](CSSpseudo-classselectors.md)
>- [Pseudo-elements selectors](CSSpseudo-elementsselectors.md)
>- [Attribute selectors](CSSattributeselectors.md)

<center><h2>Basic CSS Selectors</h2></center>

### CSS element Selector
- selects HTML elements based on the element name.
```CSS
p {
	text-align: center;
	color: red;
}
```
>[!WARNING] An ID name cannot start with a number!

### CSS id Selector
- uses the ID attribute of an HTML element to select a specific element.
- The ID of an element is unique within a page, so the ID selector is used to select one unique element
	- To select an element with a specific id, write a hash(#) character, followed by the id of the element.
```CSS
#para1 {
	text-align: center;
	color: red;
}
```

### CSS class Selector
- selects HTML elements with a specific class attribute.
	- to select elements with a specific class, write a period (.) character, followed by the class name.
```CSS
.center {
	text-align: center;
	color: red;
}
```
>[!FAQ] You can also specify that only specific HTML elements should be affected by a class.

- HTML elements can also refer to more than one class
```CSS
	<p class="center large">This paragraph refers to two classes.</p>
```
>[!WARNING] A class name cannot start with a number!

### CSS Universal Selector
- this universal selector (**\***) selects all HTML elements on the page.
```CSS
* {
	text-align: center;
	color: blue;
}
```

### CSS Grouping Selector
- selects all the HTML elements with the same style definitions.
```CSS
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```
>[!FAQ]- It will be better to group the selectors, to minimize the code.
> To group selectors, seperate each selector with a comma.

---
## ALL CSS Simple Selectors

| **Selector**         | **Example**      | **Example description**                          |
| -------------------- | ------------ | -------------------------------------------- |
| [`#id`](CSSidselector.md)                  | `#firstname` | Selects the element with id="firstname"      |
| .[class](CSSclass.md)               | .intro       | Selects all elements with class="intro"      |
| [element.class](CSSelement.class.md)        | p.intro      | Selects only <p> elements with class="intro" |
| [*](CSSallselector.md)                    | *            | Selects all elements                         |
| [element](CSSelement.md)              | p            | Selects all `<p>` elements                   |
| [element, element, ..](CSSelementelement.md) | div, p       | Selects all `<div>` elements and all `<p>` elements                                             |
