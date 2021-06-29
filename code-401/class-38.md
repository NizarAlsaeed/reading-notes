# React 2

Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like 
if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

### Conditional Rendering
```js
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {    return <UserGreeting />;  }  return <GuestGreeting />;}
ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,  document.getElementById('root'));
```

### Lists and Keys
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a <li> element for each item.
```js
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>  <li>{number}</li>);
```

Keys help React identify which items have changed, are added, or are removed. Keys 
*should be given to the elements inside the array to give the elements a stable identity.

### Forms
In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state 
and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. 
An input form element whose value is controlled by React in this way is called a “controlled component”
