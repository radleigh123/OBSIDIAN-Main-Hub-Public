---
aliases:
tags:
- HTML
---
**[[HTMLtables#HTML Table Tags|BACK]]**

---
## Table Column element `<col>` & Table Column Group element `<colgroup>`
 It is useful for applying styles to entire columns, instead of repeating the styles for each cell, for each row.
>[!column|flex no-t]
>>[!NOTE|collapse ttl-c clean no-i] `<colgroup>`
>> tag specifies a group of one or more columns in a table for formatting.
>
>>[!NOTE|collapse ttl-c clean no-i] `<col>`
>> tag specifies column properties for each column within a `<colgroup>`element.

```HTML
<table>
    <caption>Superheros and sidekicks</caption>
    <colgroup>
        <col>
        <col span="2" class="batman">
        <col span="2" class="flash">
    </colgroup>
    <tr>
        <td> </td>
        <th scope="col">Batman</th>
        <th scope="col">Robin</th>
        <th scope="col">The Flash</th>
        <th scope="col">Kid Flash</th>
    </tr>
    <tr>
        <th scope="row">Skill</th>
        <td>Smarts</td>
        <td>Dex, acrobat</td>
        <td>Super speed</td>
        <td>Super speed</td>
    </tr>
</table>
```
![[Pasted image 20221124231344.png|center cover wm-tl]]
```CSS
.batman {
    background-color: #d7d9f2;
}

.flash {
    background-color: #ffe8d4;
}

caption {
    padding: 8px;
    caption-side: bottom;
}

table {
    border-collapse: collapse;
    border: 2px solid rgb(100, 100, 100);
    letter-spacing: 1px;
    font-family: sans-serif;
    font-size: .7rem;
}

td,
th {
    border: 1px solid rgb(100, 100, 100);
    padding: 10px 10px;
}

td {
    text-align: center;
}
```
# 

<br>

---
**Sources:**
- [<colgroup>: The Table Column Group element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup)
- [HTML colgroup tag (w3schools.com)](https://www.w3schools.com/tags/tag_colgroup.asp)