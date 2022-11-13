**[[WEBDEV11LEC#^SEMICH2|BACK]]**

---
## Borders
- The **`border`** properties specify the appearance of an element's border on a web page.
	- CSS **`border`** properties specify the *style*, *size*, and *color* of an HTML element's border. These are as follows:
		- **`border-color`** specifies the color of a border.
		- **`border-style`** specifies the kind of border to display either *dashed*, *dotted*, *solid* or *none*.
		- **`border-width`** specifies the width of a border.

```HTML CSS
<!DOCTYPE html>
<html lang="en">
	<head>
		<style>
			.borders {
				border-width: 5px;
				border-color: red green blue yellow;
				border-style: dotted solid;
				border-radius: 10px;
			}
		</style>
	</head>
	<body>
		<p class="borders">Adding styles to an HTML element's border using CSS border properties.</p>
	</body>
</html>
```

---
## Outlines
- An **`outline`** is a line outside an HTML element's border to make an HTML element stand out.
- CSS **`outline`** properties specify the *style*, *size*, and *color* of an HTML element's outline. These are as follows:
	- **`outline-width`** defines the width of an outline
	- **`outline-style`** determines whether the line style of an outline is *solid*, *dashed*, *dotted* or *none*.
	- **`outline-color`** specifies the color of an outline.

```HTML CSS
<!DOCTYPE html>
<html>
    <head>
        <style>
            .design {
                outline-style: dashed;
                outline-color: blue;
                outline-width: 8px;
                outline-offset: 5px;
                border: 3px solid red;  
            }
        </style>
    </head>
    <body>
        <p class = "design">Adding styles to an HTML border using CSS border and outline properties.</p>
    </body>
</html>
```