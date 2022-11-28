---
aliases:
tags:
- HTML/Content/Flow
- HTML/Content/Phrasing
---
**[[HTMLimages#HTML Image Tags|BACK]]**

---
## Image Map element `<map>`
The `<map>` HTML element is used with [[HTMLarea|<area>]] elements to define an image map (a clickable link area).
**e.g**
```HTML
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">  
<map name="workmap">  
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">  
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">  
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">  
</map>
```

---
**Create Image Map**
>[!aside|show-title]+ Syntax:
> ```HTML
> <map name="sampleMap">
> ```

The `<map>` element is used to create an image map, and is linked to the image by using the required `name` attribute.
> The `name` attribute must have the same value as the `<img>`'s `usemap` attribute .

**The Areas**
A clickable area is defined using an [[HTMLarea|<area>]] element. ^4ea922
- **[[HTMLAREArect|rect]]** - defines a rectangular region ^50647b
- **[[HTMLAREAcircle|circle]]** - defines a circular region ^dd4dfe
- **[[HTMLAREApolygon|poly]]** - defines a polygonal region ^cc628e
- **default** - defines the entire region

# 

<br>

---
**Sources:**
- [<map>: The Image Map element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map)
- [HTML Image Maps (w3schools.com)](https://www.w3schools.com/html/html_images_imagemap.asp)