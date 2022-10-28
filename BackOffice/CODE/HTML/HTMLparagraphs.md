---
title: Paragraphs
creation-date: 2022-10-27
aliases: [paragraphs, block-level elements]
tags:
- HTML/Elements/Block-level
- HTML/Content/Flow 
---
**[[HTML#^HTMLparagraphs|HOME [HTML]]]**

---
# Paragraphs
> A paragraph always starts on a new line, and is usually a block of text.

## HTML Paragraphs
The HTML **`<p>`** element defines a paragraph.
A paragraph always <mark class="hltr-blue">starts on a new line</mark>, and browsers automatically <mark class="hltr-blue">add</mark> some <mark class="hltr-blue">white space</mark> (a margin) before and after a paragraph.
```HTML
<p>This is a paragraph</p>
<p>This is another paragraph</p>
```

>[!WARNING]- You cannot be sure how<u> HTML will be displayed</u>
> With HTML, you cannot change the display by adding extra spaces or extra lines in your HTML code.
> ```HTML
> <p>
> This paragraph
> contains a lot of lines
> in the source code,
> but the browser
> ignores it.
> </p>
> 
> <p>
This paragraph
contains         a lot of spaces
in the source         code,
but the        browser
ignores it.
> </p>
> ```

# 

<br>

---
**Sources:**
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p