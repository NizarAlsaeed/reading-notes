# Docs for the HTML \<canvas\> Element & Chart.js

## Chart.js

to implement charts in your website use this library, it makes charts a lot easier
and cotains multiple types of charts including:
1. line chart
2.  pie chart
3. bar chart

to use this library:
```html
<script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
```

## HTML \<canvas\> Element

it is used to draw diagrams on the website, to use the element:
```js
var canvas = document.getElementById('canvasId');
var ctx = canvas.getContext('2d');
```

how to draw on the canvas?
```js
fillRect(x, y, width, height)
    //Draws a filled rectangle.
strokeRect(x, y, width, height)
   // Draws a rectangular outline.

   //x and y specify the position
```
#### Drawing paths
 To make shapes using paths, we take some extra steps:

1. First, you create the path. 
2. use drawing commands to draw into the path.
3. stroke or fill the path to render it.


For drawing straight lines, use the `lineTo()` method.

```js
lineTo(x, y)
```


#### Drawing text

```js
fillText(text, x, y [, maxWidth])
```

#### fill style
use the fill style properity to change the color
```js
   ctx.fillStyle = 'rgb(255, 221, 0)';
```