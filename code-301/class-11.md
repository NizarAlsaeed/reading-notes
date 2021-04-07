# EJS


EJS is a simple templating language that lets you generate HTML markup with plain JavaScript.


## Using EJS:

**Set us yur files**
```js
- views //folder called views which contains the ejs stuff
----- partials  //code that will be reused on multiple pages
---------- footer.ejs
---------- head.ejs
---------- header.ejs
----- pages //website pages
---------- index.ejs
---------- about.ejs
- package.json
- server.js
```
1.
```js
// set the view engine to ejs
app.set('view engine', 'ejs');
```

2.
```js
// use res.render to load up an ejs view file

// index page
app.get('/', function(req, res) {
    res.render('pages/index');
});
```
>It is important to note that res.render() will look in a views folder for the view. So we only have to define pages/index since the full path is views/pages/index.
3.
```js
Use <%- include('RELATIVE/PATH/TO/FILE') %> to embed an EJS partial in another file.
```

4.
```js
To echo a single variable, we just use <%= tagline %>
```

5.
```js
//To loop over our data
/* <% for(let i=0,i<arr.length,i++>){ %>
    //code
<%}%> */
```
