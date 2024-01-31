# ![Building Your First React App - Conditional Rendering](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Conditional rendering

JavaScript provides many tools for handling conditional logic, but not all work in JSX. For example, let's say that we wanted to add a "Task Completed" prefix to our `<p>` tag if `todo.done` is true. We might think to use an `if...else` statement, like this:  

```jsx
const App = () => {
  const todo = { text: 'A brand new task', done: true };

  return (
    <>
      <h1>JavaScript in JSX</h1>
      <p>{todo.text}</p>

      <h2>Conditional Rendering</h2>
      <p>{if(todo.done) {
        'Task Completed' - todo.text
      } else {
        todo.text
      }}</p>
    </>
  );
};

export default App;
```

As we've discussed, we can't use statements in JSX. `if` statements and `if...else` statements are (as their name suggests) statements! 

So we need a way to conditionally carry out action in a way that isn't a statement. This narrows our choices a bit, but it also helps us write more concise and readable code. Check out how a ternary expression helps us accomplish our goal with this code:

```jsx
const App = () => {
  const todo = { text: 'A brand new task', done: true };

  return (
    <>
      <h1>JavaScript in JSX</h1>
      <p>{todo.text}</p>

      <h2>Conditional Rendering</h2>
      <p>{todo.done ? 'Task Completed - ' todo.text : todo.text }</p>
    </>
  );
};

export default App;
```

Ternary expressions evaluate to a single value regardless of their outcome!
