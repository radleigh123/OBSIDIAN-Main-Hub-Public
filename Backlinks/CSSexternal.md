**[BACK](CSShowto.md)**

#CSS 
## External CSS
- Each HTML page must include a reference to the external style sheet file inside the <link> element, inside the head section.
```HTML
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

- An **external style sheet** can be written in any text editor, and must be saved with a .css extension.
	- The external **.css file** should not contain any HTML tags.
```CSS
<-- "mystyle.css" -->

body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```
>[!WARNING] Note:
> Do not add a space between the property value and the unit:  
>>[!FAIL] Incorrect (space): `margin-left: 20 px;`
>
>
>>[!CHECK] Correct (nospace): `margin-left: 20px;`