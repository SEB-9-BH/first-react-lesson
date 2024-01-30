# ![Building Your First React App - Getting Started with React](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Getting Started with React

You just built your first React app! Congrats! We used a tool called Vite to help accomplish this. Here's how they describe it in their own words:

> Vite (French word for "quick", pronounced like "veet") is a build tool that aims to provide a faster and leaner development experience for modern web projects.

Build tools can accomplish a lot, but in brief Vite gives us a couple of essential capabilities:

- A starting file structure with sensible defaults.
- A development server that serves our application locally.

## Default file structure

Let's explore some of the files we have set up in our app already. The entry point into our application is the `index.html` file located in the root of our project. You can see it's contents below:

```html
<!-- index.html -->

<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite + React</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

The `index.html` file represents the entirety of the HTML we deliver to users of this application. It has some familiar boilerplate, and two elements in the body - a `<div>` with an `id` of `"root"` and a `<script>` that calls the `src/main.jsx` file. Let's check that out:

```jsx
// src/main.jsx

import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

In our `index.html`, Vite established a `<div>` with an id of `"root"`. This HTML element is important because it establishes the root of our React application as shown in this line: 

```jsx
ReactDOM.createRoot(document.getElementById('root'))
```

Passing the DOM element to `ReactDOM.createRoot()` means that React will create a `root` for this DOM element. React calls this a "root" DOM node because everything inside it will be managed by React DOM. Our app will exist inside of this element, and nothing but React should interact with anything inside of it.

`root` has methods such as `render`, which allow us to display rendered React content.

This means we can pass React components to `root.render()` like so:

```jsx
ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

The React `root` is now basically just rendering a single `App` component (ignore the `React.StrictMode` element for now), which is being imported from `src/App.jsx`: 

```jsx
// src/App.jsx

const App = () => {

  return (
    <h1>Hello world!</h1>
  );
}

export default App
```

You can begin to see how the pieces of this app are interacting with one another. The `index.html` file loads the `main.jsx` file as the entry point to our React application, which itself is rendering the `App` component.

[tktk Hunter, a graphic showing the above ^^ would be suuuuuper swell here]

## Running the development server

To start the development server and view our app in the browser, we'll use the following command: 

```bash
npm run dev
```

You should see that `Vite` is available on port number 5173: 

```plaintext
localhost:5173
```

Navigate there, and you should see the `<h1>` from our `App.jsx` component displayed!

## Other files

There are a few other files and directories that Vite created for us when we created this project. Some will potentially be familiar to you, while others will not. In the project root we have:

- `public` directory - for holding static files, such as images, served by your application.
- `.eslintrc.cjs` - for syntax highlighting to inform you of warnings or errors.
- `.gitignore` - for ensuring we don't send environment details to GitHub.
- ``

