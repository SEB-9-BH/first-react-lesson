# ![Building Your First React App - Conditional Rendering In Loops](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Conditional Rendering In Loops

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

  return (
    <>
      <h1>JavaScript in JSX</h1>
      <p>{todo.text}</p>

      <h2>Conditional Rendering</h2>
      <p>{todo.done ? 'Task Completed - ' todo.text : todo.text }</p>

      <h2>Looping With JSX</h2>
      <ul>
        {todos.map((element, index) =>
          <li key={index}>
            {element.text}
          </li>
        )}
      </ul>

      <h2>Looping And Conditional Rendering</h2>
      <ul>
        {todos.map((element, index) => 
          <li key={index}>
            {element.done ? 'Task Completed - ' : ''}{element.text}
          </li>
        )}
      </ul>
    </>
  );
}

export default App
```