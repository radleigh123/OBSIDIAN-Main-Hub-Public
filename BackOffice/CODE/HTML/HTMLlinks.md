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
**[[HTML|HOME [HTML]]]**

---
## Links
>*A link does not have to be text. A link can be an image or any other HTML element!*

<br>

### [[HTMLanchor|`<a>`]] anchor element
>[!aside|show-title bg-purple]+ Syntax
> ```HTML
> <a href="url.com">link text</a>
> ```

By default, links will appear as follows in all browsers:
- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red

>[!INFO|no-i ttl-c alt-co]  Links can of course be <u>styled with CSS</u>, to get another look!

<br>

---
### [[HTMLtarget|`target`]] attribute
>[!aside|bg-purple show-title]+ Example
> ```HTML
> <a href="https://www.google.com/" target="_blank">Sample Name</a>
> ```

it specifies where to open the linked URL, can have one of the following values:
- `_self`: Default. Opens the document in the same window/tab as it was clicked
- `_blank`: Opens the document in a new window/tab
- `_parent`: Opens the document in the parent frame
- `_top`: Opens the document in the full body of the window

Absolute URLs vs. Relative URLs
Absolute URL - Full web address, in the `href` attribute
Relative URL - Local link, a link to a page within the same website (w/out the "https://www" part)
```HTML
<!-- Absolute URL --->
<p><a href="https://www.google.org/">Goggles</a></p>

<!-- Relative URL --->
<p><a href="/css/default.asp">Go Home</a></p>
```

Image Links
To use an image as a link, just put the `<img>` tag inside the `<a>` tag
```HTML
<a href="default.asp">
<img src="image.gif" alt="a girl" style="width:50%">
</a>
```

Link to an Email Address
Use the `mailto:` inside the `href` attribute to create a link that opens the user's email program
```HTML
<a href="mailto:name@example.com">Send sauce</a>
```

Button Links
To use an HTML button as a link, you have to add some **[[JAVASCRIPT|JavaScript code]]**.
```HTML JavaScript
<button onclick="document.location='default.asp'">Sample World</button>
```

Title Links
The `title` attribute specifies extra information about an element. The information is most often shown as a tooltip text when the mouse moves over the element.
```HTML
<a href="https://www.google.com/" title="To me charot">Sample Title</a>
```

HTML Links - Different Colors
> An HTML link is displayed in a different color depending on whether it has been visited, unvisited, or active
>>[!EXAMPLE|no-i]- Sample 
>>![[20221101_1216]]

Button Links 2
> A link can also be styled as a button, by using **CSS**
>>[!EXAMPLE|no-i]- Sample
>>![[20221101_1224|no-title clean]]

HTML Links - Bookmarks
so that readers can jump to specific parts of a web page, can be useful if a web page is very long
>[!EXAMPLE|no-i]- Sample
> ![[20221101_1232|no-title clean]]

<br>

>[!done|no-i collapse] You can read more about file paths in [[HTMLfile_paths|HTML File Paths]] ^5314e2

>[!done|no-i collapse] Complete list of all HTML tags, [[HTMLtags|HTML Tag Reference]].

# 

<br>

---
- [HTML Links Hyperlinks (w3schools.com)](https://www.w3schools.com/html/html_links.asp)
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#attr-target