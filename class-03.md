# HTML Lists, CSS Boxes, JS Control Flow

## HTML Lists
>HTML & CSS Chapter 3: Lists

Three list types:
- Ordered lists 
    ```html
    <ol>
    <li></li>
    <li></li>
    </ol>
    ```
- Unordered lists 
    ```html
    <ul>
    <li></li>
    <li></li>
    </ul>
    ```
- Definition lists 

    ```html
    <dl>
    <dt>terminology</dt>
    <dd>definition</dd>
    <dt>terminology</dt>
    <dd>definition</dd>
    </dl>
    ```
    result:
    <dl>
    <dt>terminology1</dt>
    <dd>definition1</dd>
    <dt>terminology2</dt>
    <dd>definition2</dd>
    <dt>terminology3</dt>
    <dd>definition3</dd>
    </dl>
***Quiz:***How can we write a nested list?

## CSS Boxes
>HTML & CSS Chapter 13: Boxes

You can specify the width and the height of a content are using `width` and `height` properties, there is also 
1. `max-width` and `max-height` 
2. `min-width` and `min-height`

example:
```html
<div style=" max-width:200px;">
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh 
</div>
------------
<div style=" max-height:200px;">
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh 
</div>
```
<div style="max-width:200px; ">
lorem pihaj h asdfp hipad dsfpas  paisdf 
posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 
8 faksjkhdufa  usdhhmsh lorem pihaj h asdfp hipad dsfpas  paisdf 
posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 
8 faksjkhdufa  usdhhmsh 
</div>
------------
<div style=" max-height:200px;">
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh 
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh
</div>

#### overflow: hidden/scroll

when the content exceeds the container change the overflow properity.

<div style=" width:150px;height:150px; overflow:scroll;">
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh 
lorem pihaj h asdfp hipad dsfpas  paisdf posd oasdfm aoisdf hbaysg mnn a 4nnu uhe 8 faksjkhdufa  usdhhmsh
</div>

#### Border

use shorthand `border: 3px dotted #0088dd`

## JS Control Flow

Switch statement
```html
switch (mark) {
case 70:
mark= 'Good';
break;
case 80:
mark= 'V.Good';
break;
case 90:
mark= 'Excellent';
break ;
default :
break;
```