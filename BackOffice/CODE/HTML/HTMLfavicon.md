---
title: Favicon
creation-date: 2022-10-26
aliases:
tags:
- HTML/lec
---
**[[HTML#^HTMLfavicon|HOME [HTML]]]**

---
# Favicon

> A favicon is a small image displayed next to the page title in the browser tab.

## How To Add a Favicon in HTML
>[!FAQ]- TIP
>You can use any image you like as your favicon. You can also create your own favicon on sites
> [https://www.favicon.cc](https://www.favicon.cc/)

A favicon image is displayed to the left of the page title in the browser tab, like this:![[Pasted image 20221018022552.png]]

>[!INFO]- A favicon is a small image, so it should be a simple image with high contrast.

To add a favicon to your website, either save your favicon image to the root directory of your webserver, or create a folder in the root directory called images, and save your favicon image in this folder. A common name for a favicon image is "favicon.ico".

Next, add a `<link>` element to your "index.html" file, after the `<title>` element, like this:
```HTML
<!DOCTYPE html>
<html>
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
Now, save the "index.html" file and reload it in your browser. Your browser tab should now display your favicon image to the left of the page title.

## Favicon File Format Support
The following table shows the file format support for a favicon image:

| Browser | ICO | PNG | GIF | JPEG | SVG |
| ------- | --- | --- | --- | ---- | --- |
| Edge    | Y   | Y   | Y   | Y    | Y   |
| Chrome  | Y   | Y   | Y   | Y    | Y   |
| FireFox | Y   | Y   | Y   | Y    | Y   |
| Opera   | Y   | Y   | Y   | Y    | Y   |
| Safari  | Y   | Y   | Y   | Y    | Y    |

## Chapter Summary
- Use the HTML `<link>` element to insert a favicon

## HTML Link Tag

| Tag      | Description |
| -------- | ----------- |
| `<link>` | Defines the relationship between a document and an external resource            |

>[!NOTE] Note:
> For a complete list of all available HTML tags, visit our [HTML Reference (w3schools.com)](https://www.w3schools.com/tags/default.asp)