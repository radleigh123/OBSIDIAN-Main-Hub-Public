**[Home [WEBDEV]](WEBDEV11LEC.md#^MIDCH3)**

# Applying CSS
There are three ways to add CSS style rules to HTML elements. These are as follows:

-   `Inline Style` applies a unique style to a specific `HTML` element. This is done by adding the `style` attribute that contains any `CSS` property to a specific `HTML` element. In the example below, an `inline CSS` is used for the paragraph `<p>` tag. It sets the `color` and the `left margin` of the paragraph.

Code:

```
    <p style = "color:blue; margin-left:20px;"> This is a paragraph.</p>
```

Output:

This is a paragraph.

-   `Internal Style Sheet` defines the style of a single HTML document. It is defined inside the `<style>` element, in the `<head>` section of an `HTML` document. In the example below, an `internal CSS` is used to define the style rule for the `<h1>` element. It displays the text `This is h1 heading.` in `red`, `18px` font.

Code:

```
<html>
    <head>
        <style>
            h1 {  
                color: red;  
                font-size: 18px;  
            }
        </style>
    </head>

    <body>
        <h1>This is heading 1.</h1>
    </body>
</html>
```

Output:

# This is heading 1.

-   `External Style Sheet` defines the styles that are applied to many pages. It is a file that defines the style of an entire website. Any edit that you make to the file affects the style of the pages that use it. The reference to the `external CSS` file is included within the `<link>` element inside the `<head>` section of an `HTML` document.

Code:

The `HTML` document

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

The `mystyle.css` file

```
body {
    background-color: lightblue;
}

h1 {
    color: navy;
    margin-left: 20px;
}
```