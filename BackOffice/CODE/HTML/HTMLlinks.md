---
aliases: [link, target, anchor]
tags:
- HTML/Elements
- HTML/Attributes/Global_Attributes/download
- HTML/Attributes/Global_Attributes/href
- HTML/Attributes/Global_Attributes/hreflang
- HTML/Attributes/Global_Attributes/ping
- HTML/Attributes/Global_Attributes/referrerpolicy
- HTML/Attributes/Global_Attributes/rel
- HTML/Attributes/Global_Attributes/target
- HTML/Attributes/Global_Attributes/type
- HTML/Content/Flow
- HTML/Content/Phrasing
- HTML/Content/Interactive
---
**[[HTML#^HTMLlinks|HOME [HTML]]]**

---
## Links
HTML links are hyperlinks.
>[!WARNING] A link does not have to be text. A link can be an image or any other HTML element!

<br>

### `<a>` anchor element
The most important attribute of the **`<a>`** element is the **`href`** attribute, which indicates the link's destination.
By default, links will appear as follows in all browsers:
- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red
```HTML
<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
```

>[!INFO] Links can of course be styled with CSS, to get another look!

### <mark class="hltr-blue">[[HTMLtarget|target]]</mark> attribute
> specifies where to open the linked document, can have one of the following values:
```HTML
<a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a>
```
>[!INFO] `_blank`:
> usually a new tab, but users can configure browsers to open a new window instead.
>>[!NOTE] Note:
>> Setting `target="_blank"` on `<a>` elements implicitly provides the same `rel` behavior as setting `rel="noopener"` which does not set `window.opener`.

# 

<br>

---
- [HTML Links Hyperlinks (w3schools.com)](https://www.w3schools.com/html/html_links.asp)
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#attr-target