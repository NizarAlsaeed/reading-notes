# JS Object Literals; The DOM

## JS Object Literals

Objects group together a set of variables and functions to create a model
of a something. Inside objects variables become known as properities and functions as methods.

### creating objects
* Literal Notation
```javascript
var objectName = { 
//key: value 
properityName:value
methodName:function(){
    statements
}
} ;

``` 
* constructor notation
```javascript
var objectName = new object();
objectName.properityName = value;
objectName.methodName = function(){
    statements
}

```
## The Document Object Model (DOM)

The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window.

* accessing the nodes

individual node | multible nodes 
----------------|---------------
getElementById()|getElementsByClassName()
querySelector()|querySelectorAll()
  ــــــــــ    | getElementsByTagName()


### working with nodes

- Accessing text only
```javascript
textcontent
innertext //avoid it as it is not supported by Firefox
```
- Adding or removing HTML content
```javascript
innerHTML
createElement ()
createTextNode()
appendChild()
```

- CHECK FOR AN ATTRIBUTE
```javascript
hasAttribute()
```
- CREATING ATTRIBUTES 
```javascript
setAttribute()
```
- REMOVING ATTRIBUTES
```javascript
removeAttribute() 
```

## Understanding The Problem Domain Is The Hardest Part Of Programming

Programming is easy if you understand the problem domain

If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

1. Make the problem domain easier
2. Get better at understanding the problem domain

You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.