---
title: Attributes
creation-date: 2022-10-26
aliases:
tags:
- HTML/Basics
---
**[[HTML|HOME [HTML]]]**

---
# Attributes
- provides additional information about elements
- all HTML elements can have *attributes*
- usually come in name/value pairs like:
**`name="value"`**

## `href` Attribute
The **[`<a>`](HTMLlinks.md)** tag defines a hyperlink. The **[`href`](HTMLlinks.md)** attribute specifies the URL of the page the link goes to:
```HTML
<a href="https://www.google.com">Google</a>
```

## `src` Attribute
The **[`<img>`](HTMLimages.md)** tag is used to embed an image in an HTML page. The **`src`** attribute specifies the path to the image to be displayed.
```HTML
<img src="image.png">
```
2 ways to specify the URL in the **`src`** attribute:
- **[Absolute URL](HTMLATTRIBUTEabsoluteurl.md)** ^ABSOLUTEURL
- **[Relative URL](HTMLATTRIBUTErelativeurl.md)** ^RELATIVEURL

## `width` & `height` Attribute
The **[`<img>`](HTMLimages.md)** tag should also contain the **`width`** and **`height`** attributes, which specify the width and height of the image (in pixels):
```HTML
<img src="img_boy.jpeg" width="500" heigh="600">
```

## `alt` Attribute
The required **`alt`** attribute for the **[`<img>`](HTMLimages.md)** tag specifies an alternate text for an image, if the image for some reason cannot be displayed.
```HTML
<img src="img_boy.jpeg" alt="Image of a boy">
```

## `style` Attribute
The **[`style`](HTMLstyles.md)** attribute is used to add styles to an element, such as color, font, size, and more.
```HTML
<p style="color: red;">A red paragraph</p>
```

## `lang` Attribute
You should always include the **`lang`** attribute inside the **`html`** tag, to declare the language of the Web page. 
This is meant to assist *search engines* and *browsers*.
```HTML
<!DOCTYPE html>
<html lang="en">
<body>
...
</body>
</html>
```

>[!NOTE]- Country codes can also be added to the language code in the ***lang*** attribute
>![[Pasted image 20221022150622.png]]

You can see all the language codes in our [HTML Language Code Reference](https://www.w3schools.com/tags/ref_language_codes.asp)

## `title` Attribute
The **`title`** attribute defines some extra information about an element. The value of the title attribute will be displayed as a tooltip when you mouse over the element:
```HTML
<p title="I'm a tooltip">This is a paragraph</p>
```

>[!WARNING]-
>- Always use lowercase attributes
>	- **`<title>`**
>- Always quote attribute values
>	- **`<img src="img_boy.jpg">`**

# 

<br>

---
**Sources:**
- [HTML Attributes (w3schools.com)](https://www.w3schools.com/html/html_attributes.asp)

**Attribute References:**
- [HTML Attribute Reference (w3schools.com)](https://www.w3schools.com/tags/ref_attributes.asp)