# Flexbox and Templating

## Javascript Templating

the idea is to render client-side view templates with Javascript by using a JSON data source.

```html
<!-- in your HTML File -->
<h1> hello {{name}}</h1>

<!--then
to render client-side view templates with Javascript by using a JSON data source.
 res.render(TEMPLATE_NAME, JSON_DATA)

TEMPLATE_NAME is the file name without extension    

ex: res.render('index', {"name": "nizar"})
-->
```

## Flexbox

### Flexbox properties

**Properties for the Parent
(flex container)**

-   `display: flex; /* or inline-flex */`
-    `flex-direction: row | row-reverse | column | column-reverse;`
-   `.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}`

    nowrap (default): all flex items will be on one line
    wrap: flex items will wrap onto multiple lines, from top to bottom.
    wrap-reverse: flex items will wrap onto multiple lines from bottom to top.

-   `  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;`

-   `  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;`

  
-   `  align-content: /*the same values for align-items*/` This aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.

> This property only takes effect on multi-line flexible containers, where flex-flow is set to either wrap or wrap-reverse). A single-line flexible container (i.e. where flex-flow is set to its default value, no-wrap) will not reflect align-content.

**Properties for the Children
(flex items)**

-   `  order: 5; /* default is 0 */`
-   `  flex-grow: 4; /* default 0 */` 
This defines the ability for a flex item to grow if necessary. If one of the children has a value of 2, the remaining space would take up twice as much space as the others (or it will try to, at least).
-   `flex-shrink` the opposite of `flex-grow`
-   `align-self: auto | flex-start | flex-end | center | baseline | stretch;` This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.