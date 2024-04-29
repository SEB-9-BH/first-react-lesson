# ![Building Your First React App - Function Components](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to create and export function components in React.

## Function components

React components are essentially JavaScript functions that let you combine markup, CSS, and JavaScript into reusable UI elements. When crafting larger applications, React's approach to components allows us to write significantly more manageable code.

We've already created the `App.jsx` function component, but let's take a step back and break down the process of creating a new component from scratch using `App` as our example.

### Step 1: Define the function

The first step when creating a function component is to define the function. React function components are composed in exactly the same way as normal JavaScript functions:

```jsx
const App = () => {};
```

> 🧠 From the React Docs: 'React components are regular JavaScript functions, but their names must start with a capital letter or they won't work!'

### Step 2: Add markup

Next, we add the markup inside of the `return` statement of the function. Here we have an `<h1>` element with the text content `Hello world!`.

```jsx
return <h1>Hello world!</h1>;
```

> 🧠 Markup inside of the `return` statement is what will be displayed to the user.

Note that the markup we add goes inside of a `return`. It is also surrounded by `( )` because we've split what will be returned across multiple lines. Without the parenthesis, code on lines after the `return` would be ignored.

### Step 3: Export the function

React uses [ES Module](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) syntax for importing and exporting files. `export default` allows us to denote a main function in a file to export, which can then be imported in other files.

```jsx
const App = () => {
  return <h1>Hello world!</h1>;
};
// Add the below line of code:
export default App;
```

### Step 4: Importing/using the component

With the component exported we can now use it anywhere in our application. We're already importing and using it in the `src/main.jsx` file, let's check it out:

```jsx
// src/main.jsx

import React from 'react';
import ReactDOM from 'react-dom/client';
// We import the default export from App.jsx.
// We can name the function whatever we want here, so we'll call it 'App'
import App from './App.jsx';
import './index.css';

// We use the component below. Note that the tag is self-closing.
ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```
