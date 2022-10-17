| **[[CSS]]** | **[[CSSselectors]]** | 
| ------- | ---------------- |

#CSS #CSSlec #CSSselectors 
## Combinator Selectors
>[!INFO] A <u>combinator</u> is something that explains the relationship between the selectors.

A CSS selector can contain more than one simple selector. Between the simple selectors, we can include a combinator. There are 4 different combinators in CSS:
>[!EXAMPLE]- descendant selector (space)
> The descendant selector matches all elements that are descendants of a specified element.
> ```CSS
> div p {
> 	background-color: yellow;
> }
> ```

>[!EXAMPLE]- child selector (>)
> The child selector selects all elements that are the children of a specified element.
> ```CSS
> div > p {
> 	background-color: yellow;
> }
> ```

>[!EXAMPLE]- adjacent sibling selector (+)
> The adjacent sibling selector is used to select an **element that is directly after another specific element**.
> Sibling elements must have the same parent element, and "adjacent" means "**immediately following**".
> ```CSS
> div + p {
> 	background=color: yellow;
> }
> ```

>[!EXAMPLE]- general sibling selector (~)
> The general sibling selector selects all elements that are next siblings of a specified element.
> ```CSS
> div ~ p {
> 	background-color: yellow;
> }
> ```