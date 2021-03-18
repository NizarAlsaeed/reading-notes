# HTML Links, CSS Layout, JS Functions

## HTML Links
To insert a link in your website use`<a href="http://www.example.com">This is a link</a>`

you can change the `href` to indicate to a local page like`about-us.html` or to a section inside the website using the element id like this:
```html
<a href="#scale">go to scaling section</a>

<section id="scale"></section>
```
for emails use `<a href="mailto:em@example.org">Email us</a>`

by using the target attribute added to th `a` element you can open the link n a new tab `target="_blank"`

- ***Quiz***: can you link to a specifc section in another page? how?

## CSS Layout

Elements are of two types; either `block` or `inline` by default.
an `inline` means the element takes only the required space and sits beside other elements, on the other hand `block` elements takes all the horizontal space and sits in a new line.

CSS has the following positioning schemes:
1. Normal flow
    - normal flow means it is displayed as normal or default place based on it's type(either`inline` or `block`)
    ```css
    position:static;
    ```
2. Relative Positioning
    - relative means it is positioned relative to the normal position
    ```css
    position:relative;
    ```
3. Absolute positioning
    - means it is positioned relative to the page only disregarding any parents or childs elements.
    ```css
    position:absolute;
    ```
    - there is other positioning ways,such as:
    ```css
    position:fixed
    ```
    here the element is fixed regardless of ant scrolling in the page.

- `z-index:<number>;` this controlls the layer of the element
- i suggest to not use `float` it will mess up the page when any unexpected error happens.

The screen sizes are different from phone, tablet to the laptop, your website should take this into account, the website either will be *fixed-layout* which is fixed regardless of the window size, and *liquid-layout* which is resizes itself based on the window size

## JS Functions


functions are series of statements or le us say a section of code gruped together in the same block and referenced with a name, whenever you want to run this code you can do what we call it a function call.

functions might return a value but it is not necessary, they may just do a specific task that happens recurrsvely in our program.


#### define a function

```javascript
function nameoffunction(parameter1,parameter2){
    section of code
}
```

#### calling a function
```javascript
nameoffunction(argument1,argument2);
```

#### Anonymous functions
a function whithout a name but it is stored in a variable

```javascript
var squared = function(x) {
return x * x;
} ;
var y = squared(3); // y = 9
```

- There are two types of variables in regarding to the scope;
    -   local variable: works inside the block only
    -   global variable: accessable anywhere in the code sheet.

### 6 Reasons for Pair Programming
pair programming is when you work with anothe collegue on the same project while one is coding and the other is thincking and supporting the coder, this way your code will be more efficient and you will gain new skills quicker. 
1. Greater efficiency
2. Engaged collaboration
3. Learning from fellow students
4. Social skills
5. Job interview readiness
6. Work environment readiness

see https://gitduck.com/ which is a website for pair programming it mght be helpful.