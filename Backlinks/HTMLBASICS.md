**[HTML](HTML#^HTMLbasics)**

#HTML 
# The Basics
>[!TIP] ## HTML Documents
>- All HTML documents must start with a document type declaration: `<!DOCTYPE html>`
>- The HTML document itself begins with `<html>` and ends with `</html>`
>- The visible part of the HTML document is between `<body>` and `</body>`
> 
> >[!EXAMPLE]
> >![[Pasted image 20221013222131.png]]

>[!TIP] The **<!DOCTYPE>** declaration
>- The `<!DOCTYPE>` declaration represents the document type, and helps browsers to display web pages correctly.
>- It must only appear once, at the top of the page (before any HTML tags).
>	- The `<!DOCTYPE>` declaration is not case sensitive.
>	- The `<!DOCTYPE>` declaration for HTML5 is:
>
> ![[Pasted image 20221013222403.png]]

>[!TIP] Headings
> `<h1>` defines the most important heading. `<h6>` defines the least important heading:
> ![[Pasted image 20221013222450.png]]

>[!TIP] Paragraphs
>![[Pasted image 20221013222543.png]]

>[!TIP] Links
>![[Pasted image 20221013222617.png]]

>[!TIP] Images
> The source file (`src`), alternative text (`alt`), `width`, and `height` are provided as attributes:
> ![[Pasted image 20221013222753.png]]

>[!INFO] How to view HTML Source
>>[!EXAMPLE] #### View HTML Source Code
>> Right-click in an HTML page and select "View Page Source" (in Chrome) or "View Source" (in Edge), or similar in other browsers. This will open a window containing the HTML source code of the page.
>
>>[!EXAMPLE] Inspect HTML Element
>> Right-click on an element (or a blank area), and choose "Inspect" or "Inspect Element" to see what elements are made up of (you will see both the HTML and the CSS). You can also edit the HTML or CSS on-the-fly in the Elements or Styles panel that opens.