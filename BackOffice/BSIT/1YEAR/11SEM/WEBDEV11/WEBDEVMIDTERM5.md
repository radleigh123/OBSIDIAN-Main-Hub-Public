**[Home [WEBDEV]](WEBDEV11LEC.md#^MIDCH5)**

# Working with Images
Images can enhance the design, appearance, and feel of a web page. CSS image properties play an important role to control the appearance of an image on a web page.

CSS image properties define the `border`, `height`, and `width` of an image.

Code:

```
<!DOCTYPE html>
<html>
    <head>
        <style>
            img {
                border: 3px dashed red;
                height: 50px;
                width: 200px;
            }
        </style>
    </head>

    <body>
        <img src="/static/images/logo.png">
    </body>
</html>
```

![](https://universityofcebu.ethinksites.com/pluginfile.php/1463981/mod_page/content/5/image.png)  

  

The code above breaks down as follows:

-   `border: 3px dashed red;` sets the `border` of an image to `3px dashed red`.
    
-   `height: 50px;` sets the `height` of an image to `50px`.
    
-   `width: 200px;` sets the `width` of an image to `200px`.
    
-   `<img src="/static/images/logo.png">` the `<img>` element displays the image `logo.png` on the browser window.