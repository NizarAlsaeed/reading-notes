# React
## JSX
After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions.

By default, React DOM escapes any values embedded in JSX before
rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. 
Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.

### Rendering
React elements are immutable. Once you create an element, you can’t change its children or attributes.

Elements can represent user-defined components,For example, this code renders “Hello, Sara” on the page:
```js
function Welcome(props) {  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;ReactDOM.render(
  element,
  document.getElementById('root')
);
```
## Next.js
Next.js is a React framework that is bound to ease your life as a React developer by abstracting away the common and redundant tasks.



## Tailwind
With Tailwind, you style elements by applying pre-existing classes directly in your HTML.

benefits:

- You aren’t wasting energy inventing class names. No more adding silly class names like sidebar-inner-wrapper just to be 
able to style something, and no more agonizing over the perfect abstract name for something that’s really just a flex container.
- Your CSS stops growing. Using a traditional approach, your CSS files get bigger every time you add a new feature.
With utilities, everything is reusable so you rarely need to write new CSS.
- Making changes feels safer. CSS is global and you never know what you’re breaking when you make a change. 
Classes in your HTML are local, so you can change them without worrying about something else breaking.
