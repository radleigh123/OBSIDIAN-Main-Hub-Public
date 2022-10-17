| **[[CSS]]** | **[[CSSselectors]]** | 
| ------- | ---------------- |

#CSS #CSSlec #CSSselectors 
## CSS Pseduo-classes
>[!INFO]- A pseduo-class is used to define a special state of an element. 
> For example, it can be used to:
>- Style an element when a user mouses over it
>- Style visited and unvisited links differently
>- Style an element when it gets focus
>
> ![[Pasted image 20221018011543.png]]

>[!INFO]- Syntax
> ```CSS
> selector:pseudo-class {
> 	property: value;
> }
> ```

### Anchor Pseduo-classses
Links can be displayed in different ways:
```CSS
/* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}
```
>[!WARNING] Note:
> **a:hover** MUST come after **a:link** and **a:visited** in the CSS definition in order to be effective! **a:active** MUST come after **a:hover** in the CSS definition in order to be effective! Pseudo-class names are not case-sensitive.