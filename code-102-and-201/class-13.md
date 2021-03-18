# Local Storage


 **HTML5 Storage**

 it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server.

 HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. 

to deal with the localStorage object use `getItem()` and `setItem()`
```js
 var foo = localStorage.getItem("bar");
localStorage.setItem("bar", foo);
```
Also, it could be rewritten to use square bracket syntax instead:
```js
var foo = localStorage["bar"];
localStorage["bar"] = foo;
```


If you want to keep track programmatically of when the storage area changes, you can use the storage event. `addEventListener('storage',func);`

#### Limitations in Current Browsers

5 megabytes is how much storage space each origin gets by default. and you can not expand it in most browsers

