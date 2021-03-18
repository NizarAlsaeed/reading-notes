# HTML Text, CSS Introduction, and Basic JavaScript Instructions


## HTML Text
### Text Elements
> HTML & CSS Chapter 2:Text
- Headings
use the headings to emphasize the importance of the text
```html
<h1></h1>
.
.
<h6></h6>
```
-Paragraphs`<p></p>`
- bold and italic
`<b></b>` `<i></i>`
- Superscript and subscript
```html
<p> H<sub>2</sub> O
Y =X<sup>2</sup></p>
```
- Line Breaks & Horizontal Rules
```html
<p> Some Text <br /> another text to be on the next line</p>
<!--horizontal rules-->
<p></p>
<hr />
<p></p>
```

##### Semantic elements
- Strong & Emphasis`<strong></strong>` and`<em></em>`
- quotations `<blockquote><p> Text</p></blockquote>` and <q>Text</q>
- citation `<p><cite></cite></p>`

***Quiz:*** what is the main difference between the six heading elements?

## CSS Introduction
CSS is an abbreviation of Cascading Style Sheet, it is a scripting language used to give a style to the html elements and make the web page more readable and adds beauty to it.

* CSS Properties Affect How Elements Are Displayed
```css
Element
---
div{
   
    font-style:italic;
    ---------- ------
     property   Value
}
```
* Three ways of styling:
1. inline style
2. internal style
3. external style

## Basic JavaScript

### Variables
use var or let to declare variables, the are approximately the same except for a small difference to be discussed later.
```javascript
var userName = 'ALI';
let age = 25;
```
### Arrays

An array is a special type of variable. It doesn't
just store one value; it stores a list of values.
```javascript
var userNames = ['ALI','Ibrahim', 'Mohannad'];
let ages = [25,26,27];

// index   value
// 0       ALI
// 1       Ibrahim
// 2       Mohannad

var x= ages[1]; //x=26
```
### Loops and operators in Javascript

#### Comparison operators
- `==` is equal to
- `!=` is not equal to
- `===` strict equal to
- `!==` strict not equal to
- `>` Greater than `>=` Greater than or equal
- `<` Less than and `<=` Less than or equal


#### Logical operators
- `&&` Logical And
- `||` Logical OR
- `!` Logical Not
> Logical Operators are evaluated *left* to *right*.
If the first condition can provide enough information to get the answer, then there is no need to evaluate the second condtion.

#### Loops
Loops check a condition if it returns true, a code block will run untill it returns false.

##### for loop
```javascript
for (var i=0; i<number,i++){
    statements;
}
```
##### while loop
```javascript
while(i<number){
    statements;
    i++;
}
```