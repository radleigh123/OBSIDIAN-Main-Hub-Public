**[HOME [WEBDEV]](WEBDEV11LEC#^MIDCH1)**

# Basic CSS Syntax
>[!INFO]- CSS (Cascading Style Sheets)
>- is a rule-based language that applies styling to **[HTML elements](WEBDEVelements.md)**. It is used to add layout and design to a web page.

The CSS style rules can modify the appearance of a web page such as its colors, background, width, border thickness, font sizes, and font colors. CSS style rules can be applied to HTML elements like **`<p>`** and **`<img>`**.

The CSS style rule is made up of two parts:
-   **Selector** - identifies HTML elements that the style rule is applied to.
-   **Declaration block** - defines a set of declarations separated by semicolons `;` and surrounded by curly braces `{}`.

A declaration consists of two parts:
```CSS, HTML
background-color: blue
```
>[!INFO]- property: <u>background-color</u>
>- is a feature such as font, width, and background color.

>[!INFO]- value: <u>blue</u>
>- indicates how you want properties like font, width, and background color to be changed.

In the example style rule below, all **`<h1>`** elements will have **`20px`** font size and a **`red`** text color.
```CSS
h1 {
	color: red;
	font-size: 20px;
}
```