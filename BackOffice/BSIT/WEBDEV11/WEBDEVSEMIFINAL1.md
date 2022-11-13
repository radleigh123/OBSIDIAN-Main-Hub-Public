**[[WEBDEV11LEC#^SEMICH1|BACK]]**

---
# Formatting Tables
Styles can be applied to HTML tables for a better look and feel.
The appearance and behavior of tables can be defined using the different CSS table properties, such as:
-   **`border-collapse`** specifies whether table borders should appear as a single border or be separated into two borders.
-   **`border-spacing`** specifies the distance between the borders of cells that are next to each other.   
-   **`caption-side`** specifies where the caption of a table is placed.    
-   **`empty-cells`** determines whether borders and background will appear on empty cells in a table.
-   **`table-layout`** defines the layout of the table cells, rows, and columns rendered by the browser.

The example code below displays two tables with different style settings for `border-collapse`, `border-spacing`, `caption-side`, `width`, and `border` properties.
```HTML
<!DOCTYPE html>
<html>
<head>
	<style>
		table.one {
			border-collapse: separate;
			border-spacing: 15px;
			caption-side: top;
			width: 300px;
			border: 3px dashed blue;
		}
		table.two {
			border-collapse: collapse;
			border-spacing: 10px;
			caption-side: bottom;
			width: 250px;
			border: 2px solid blue;
		}
		th {
			color: white;  
			background-color: gray;    
		}
	</style>
</head>
<body>
	<table class="one">
		<caption> Table 1: Fruits </caption>
		<tr><th> Names </th></tr>
		<tr><td> Apple </td></tr>
		<tr><td> Mango </td></tr>
	</table>
	<br/>
	<table class="two">
		<caption> Table 2: Vegetables </caption>
		<tr><th> Names </th></tr>
		<tr><td> Squash </td></tr>
		<tr><td> Cucumber </td></tr>
	</table> 
</body>
</html>
```