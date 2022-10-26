**[[CSSselectors]]**

#CSS #CSS/Lecture  #CSS/Selectors 
## CSS .class Selector
**Example:** Select and style all elements with class="intro";
```CSS
.intro {
	background-color: yellow;
}
```
**Example:** HTML elements can also refer to more than one class
```CSS
<p class="center large">This paragraph refers to two classes.</p>
```

### CSS Syntax
```CSS
.class {
	css declarations;
}
```

### Definition & Usage
The `.class` selector selects elements with a specific class attribute.
To select elements with a specific class, write a period (.) character, followed by the name of the class.
You can also specify that only specific HTML elements should be affected by a class. To do this, start with the element name, then write the period (.) character, followed by the name of the class (look at Example 1 below).
```CSS
p.hometown {
	background-color: yellow;
}
```