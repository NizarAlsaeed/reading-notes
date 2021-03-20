
# SMACSS and Responsive Web Design


## Responsive Web Design


**Desfinition**

Responsive web design is the practice of building a website suitable to work on every device and every screen size.

Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media

### *Flexible Layouts*
flexible layouts, is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units

### *Media Queries*
Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example

Media Features in Media Queries
- Height & Width Media Features
- Orientation Media Feature
- Aspect Ratio Media Features
- Pixel Ratio Media Features
- Resolution Media Feature


**Viewport**
```html
<!--Using the viewport meta tag with either the height or width values will define the height or width of the viewport respectively.-->
<meta name="viewport" content="width=device-width">
<!--The initial-scale of a website should be set to 1 as this defines the ratio between the device height, while in a portrait orientation, and the viewport size-->
<meta name="viewport" content="initial-scale=1">
<!--The minimum-scale and maximum-scale values determine how small and how large a viewport may be scaled.-->
<meta name="viewport" content="minimum-scale=0">
<!--Setting the user-scalable value to no will disable any zooming-->
<meta name="viewport" content="user-scalable=yes">
<!--Using the target-densitydpi viewport value is rare, but extremely helpful when pixel by pixel control is needed.-->
<meta name="viewport" content="target-densitydpi=device-dpi">
<!--Yes you can combine them by commas-->
<meta name="viewport" content="width=device-width, initial-scale=1">
```


### *Flexible Media*

One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.

```css
img, video, canvas {
  max-width: 100%;
}
```

Flexible Embedded Media like iframes and YouTube might not work with max-width and needs a trick to make it work. Can you find the solution?

## About Floats

Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage, like when the text box in the print layout was told to ignore the page wrap. Absolutely positioned page elements will not affect the position of other elements and other elements will not affect them, whether they touch each other or not.


An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.