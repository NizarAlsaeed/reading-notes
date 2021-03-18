## CSS Layout

> Rebeat of Class 04 read

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

