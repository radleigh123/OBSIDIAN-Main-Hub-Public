---
aliases:
tags:
- HTML/Elements
- HTML/Content/Flow
- HTML/Content/Phrasing
- HTML/Content/Embedded
- HTML/Content/Palpable
- #HTML/Att
---
**[[HTML|BACK]]**

---
## Image Embed Element `<img>`
> The HTML `<img>` tag is used to embed an image in a web page.

>[!aside|show-title]+ Syntax:
> ```HTML
> <img src="globe_earth.jpg" alt="A picture">
> ```

`<img>` tag has two required attributes:
- **src** - specifies the path to the image
- **alt** - specifies an alternate text for the image

<br>

---
### `alt` Attribute
The value of the `alt` attribute should describe the image:
```HTML
<img src="image.jpg" alt="Flowers in Chania">
```

### `src` Attribute
The required `src` attribute specifies the path (URL) to the image.
>[!EXAMPLE]- Different image sources
> **Images in another folder**
> ```HTML
> <img src="/images/html5.gif" alt="HTML5 Icon">
> ```
> **Images on another server/website**
> ```HTML
> <img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">
> ```
> **Images animated**
> ```HTML
> <img src="programming.gif" alt="Computer Man">
> ```
> **Images as a [[HTMLlinks|link]]**
> ```HTML
> <a href="default.asp">  
> 	<img src="smiley.gif" alt="HTML tutorial">  
> </a>
> ```
> **Images floating**
> ```HTML
> <p>
> 	<img src="smiley.gif" alt="Smiley face" style="float:right;">  
> 	The image will float to the right of the text.
> </p>
> ```
>>[!TIP|alt-co] To learn more about CSS Float, click [[CSSfloat|CSS Float Tutorial]].

### HTML Image Tags
- [[HTMLmap|<map>]] - defines an image map
- [[HTMLmap#^4ea922|<area>]] - defines a clickable area inside an image map
- [[HTMLpicture|<picture>]] - defines a container for multiple image resources

# 

<br>

---
**Sources:**
- [HTML Image Maps (w3schools.com)](https://www.w3schools.com/html/html_images_imagemap.asp)