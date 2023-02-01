**[Home [WEBDEV]](WEBDEV11LEC.md#^MIDCH4)**

# Manipulating Fonts and Text
CSS font and text properties are used to design and manipulate the appearance of text on a web page.

Font properties are used to define the `font-family`, `boldness`, `size`, and `style` of text.

Text properties are used to define the `color`, `letter-spacing`, `text-indent`, and `direction` of text.

Code:

```
<!DOCTYPE html>
<html>
    <head>
        <style>
            p {
                font-family: Georgia;
                font-size: 20px;
                font-weight: bold;
                color: #0000ff;
                letter-spacing: 5px;
                text-transform: capitalize;
                text-shadow: 4px 4px 8px violet;
            }
        </style>
    </head>

    <body>
        <p>I love Cascading Style Sheets.</p>
    </body>
</html>
```