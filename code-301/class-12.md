# components

## EJS Partials

Partials are reusing the same HTML across multiple views.
 Under the `views/partials/` directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar.

 Now that we have our partials defined, we can use them in our `index.ejs`.

 You use `<%- include( PARTIAL_FILE ) %>` where the partial file is relative to the template you use it in. fro axample `<%- include('partials/navbar') %>`