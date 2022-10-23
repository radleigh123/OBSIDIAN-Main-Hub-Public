**[HOME [WEBDEV]](WEBDEV11LEC#^MIDCH2)**

# CSS Selectors
CSS selectors define which HTML elements a CSS style rule will apply to based on their name, id, class, attribute, and so on.

Selectors are classified into several types:
**Element Selector** - used to select HTML elements by name.
```CSS
h1 {
	color: red;
	font-size: 18px;
}
```
In the example, the selector `h1` is an example of an element selector because it uses the name of the HTML element `<h1>`. It displays the text `This is h1 heading.` in `red`, `18px` font.

**ID Selector** - used to specify a style for a single, unique element. It uses the **`id`** attribute of the HTML element and is defined with a hash sign **`#`**. To apply the style rule to the specific element, add **`id = "selector_name"`** in the HTML tag, like so: **`<h1 id = "center">This is a heading.</h1>`**.
```CSS
#center {
	text-align: center;
}
```
In the example below, **`#center`** is an id selector that specifies the **`center`** attribute of HTML elements. All elements with attributes **`id = "center"` are aligned to `center`**.

**Class Selector** - used to specify a style for a group of elements and sets a particular style for multiple HTML elements of the same class. 
```CSS
.center {
	text-align: center;
}
```
To apply style rules to elements of a specific class, write a period `.`, followed by the name of the class. To apply the style rule to the specific element, add **`class = "selector_name"`** in the HTML tag, like so: **`<h1 class = "center">This is a heading.</h1>`**.

**Universal Selector** - used to select all HTML elements on the page by using the asterisk `*` symbol as the selector.
```CSS
* {
	color: red;
	font-size: 18px;
}
```
In the example below, the text of the elements **`<h1>`**, **`<h2>`**, and **`<p>`** is rendered in the browser in **`red`**, **`18px`** font.

**Group Selector** - used to apply the same style to a number of HTML elements to minimize code. Each element selector is separated with a comma `,`.
```CSS
h1, h2, p {
	color: red;
	font-size: 18px;
}
```

In the example below, the selectors **`h1`**, **`h2`**, and **`p`** are of the same style definitions. The text of the elements **`<h1>`**, **`<h2>`**, and **`<p>`** is rendered in the browser in **`red`**, **`18px`** font.