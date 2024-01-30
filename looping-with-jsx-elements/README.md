# ![Building Your First React App - Looping with JSX Elements](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Looping with JSX Elements


Since we'll be demonstrating how to loop over JSX elements, we'll need some new data. Below `todo`, let's add the following `todos` array: 

```JSX
// src/App.jsx

  const todo = { text: 'A brand new task', done: true }
  // Add the todos array below the existing todo object.
  const todos = [
    {text: 'Learn JavaScript', done: true},
    {text: 'Learn JSX', done: false},
    {text: 'Learn HTML', done: true},
    {text: 'Learn CSS', done: true},
    {text: 'Master React', done: false},
  ]
```


```jsx
const App = () => {
  const todo = { text: 'A brand new task', done: true }
  const todos = [
    {text: 'Learn JavaScript', done: true},
    {text: 'Learn JSX', done: false},
    {text: 'Learn HTML', done: true},
    {text: 'Learn CSS', done: true},
    {text: 'Master React', done: false},
  ]

  const todoList = todos.map((element, index) =>
          <li key={index}> {element.text} </li>
        )

  return (
    <>
      <h1>JavaScript in JSX</h1>
      <p>{todo.text}</p>

      <h2>Conditional Rendering</h2>
      <p>{todo.done ? 'Task Completed - ' todo.text : todo.text }</p>

      <h2>Looping With JSX</h2>
      <ul>{todoList}</ul>
    </>
  );
}

export default App
```

Check the browser! You should see all of the todos in a list! 


<!-- Objective: Teach how to loop through data to render elements.

Topics:
Using .map() to iterate over arrays in JSX.
Key prop and its importance in lists.
Practical examples of rendering lists of data, just stick with strings or numbers for now, no need for complex data types in the array.

<https://react.dev/learn/rendering-lists>


