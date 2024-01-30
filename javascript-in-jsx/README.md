# ![Building Your First React App - JavaScript in JSX](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## JavaScript in JSX



To explore using JSX curly braces, let's create some new data. For now, let's just make a single object called `todo`:
```jsx
// src/App.jsx

const App = () => {
  // Add the following: 
  const todo = { text: 'A brand new task', done: true };

  return (
    <>
      <h1>Hello world!</h1>
      <h2>Hello universe!</h2>
      <hr />
    </>
  );
};
```

Curly braces allow us to add JavaScript to our JSX. We can write any JavaScript expression inside of the curly braces, meaning we can use dot notation to access a property on our `todo` object: 

```jsx
// src/App.jsx

const App = () => {
  const todo = { text: 'A brand new task', done: true };

  // Replace the existing return with the following: 
  return (
    <>
      <h1>JavaScript in JSX</h1>
      <p>{todo.text}</p>
    </>
  );
};

export default App
```

Inside curly braces, we can reference the `todo` object and inject the value held on its `text` property directly into our HTML-like syntax!

### Expressions vs. statements in JavaScript

Remember, we can only ever write JavaScript expressions inside of the curly braces. JavaScript expressions evaluate to a single value. They can be:

- Assigned to a variable
- Provided as an argument to a function
- Returned from a function
- `console.log()`


<!-- 
Objective: Demonstrate how to render dynamic data in JSX.

Topics:
Using JavaScript expressions to insert variable values into elements.
Handling variables and constants inside JSX.
Embedding JavaScript expressions in JSX (using curly braces {}).
Printing JS values to elements { }

<https://react.dev/learn/javascript-in-jsx-with-curly-braces> -->