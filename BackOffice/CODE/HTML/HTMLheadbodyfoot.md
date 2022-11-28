---
aliases:
tags:
- HTML
---
**[[HTMLheadbodyfoot|BACK]]**

---
The `<thead>` tag is used to group header content in an HTML table.
The `<tbody>` tag is used to group the body content in an HTML table.
The `<tfoot>` tag is used to group footer content in an HTML table.

Browsers can use these elements to enable scrolling of the table body independently of the header and footer. Also, when printing a large table that spans multiple pages, these elements can enable the table header and footer to be printed at the top and bottom of each page.

```HTML
<table>  
  <thead>  
    <tr>  
      <th>Month</th>  
      <th>Savings</th>  
    </tr>  
  </thead>  
  <tbody>  
    <tr>  
      <td>January</td>  
      <td>$100</td>  
    </tr>  
    <tr>  
      <td>February</td>  
      <td>$80</td>  
    </tr>  
  </tbody>  
  <tfoot>  
    <tr>  
      <td>Sum</td>  
      <td>$180</td>  
    </tr>  
  </tfoot>  
</table>
```
# 

<br>

---
**Sources:**
- [The Table Head element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead)
- [The Table Body element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody)
- [The Table Foot element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot)
- [HTML thead tag (w3schools.com)](https://www.w3schools.com/tags/tag_thead.asp)