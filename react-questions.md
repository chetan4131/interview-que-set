# What is the difference between npx and npm?
    - NPM is a package manager and can be used to install node.js packages.
    - NPX is a tool to execute node.js packages.

# How does react works?
    - React creates a virtual DOM. When a state chages in a component, it first runs a "diffing" algorithm which identifes what has changed in Virtual DOM. The second step is reconciliation, where it updates the dom with the result of diff.

# Explain the Virtual DOM in React.
   - The Virtual DOM is a lightweight copy of the actual DOM. React uses it to improve performance by updating only the parts of the actual DOM that have changed, rather than re-rendering the entire DOM.

# Explain  React Hooks.
    - React Hooks are functions that let you use state and other React features in functional components. 
    - In other words, hooks are the functions that make functional component work like class components.
    - (OR) Hooks provide a way to use state and lifecycle methods in functional components, which were previously only possible in class components.
# What is jsx?
JSX (JavaScript XML) is a syntax extension for JavaScript, commonly used with React to describe what the UI should look like.
1. Syntax: JSX looks similar to HTML but it is used within JavaScript code. It allows you to write HTML-like code directly in your JavaScript files.

    ```jsx
    const element = <h1>Hello, world!</h1>;
    ```
2. Purpose: JSX makes it easier to write and visualize the structure of the UI components. It allows developers to describe the UI in a more declarative way.

3. Compilation: JSX is not valid JavaScript by itself. Tools like Babel are used to transform JSX into standard JavaScript code. 

4. Embedding Expressions: JSX can include JavaScript expressions within curly braces {}. This allows you to dynamically render content based on JavaScript variables and functions.

    ```jsx
    const name = "John";
    const element = <h1>Hello, {name}!</h1>;
    ```
5. Attributes and Children: Just like HTML, you can pass attributes to JSX elements and nest child elements.

# What is the difference between a Presentational component and a Container component?

- Presentational Components
1. Purpose
    * UI Focused: These components are primarily concerned with how things look. They focus on the presentation and rendering of the UI.

2. State Management:

    * Stateless: Typically, they do not manage their own state. They receive data and callbacks exclusively via props.

# Function Components: 
    These are simple JavaScript functions that take props as input and return JSX elements. They are often used for presentational or stateless components. They do not have state or lifecycle methods directly, but with the introduction of Hooks in React 16.8, functional components can use state and other features.

# Class Components:
    These are ES6 classes that extend from React.Component or React.PureComponent and can have state and lifecycle methods. They have a render() method where you define the structure of your component's UI using JSX. Class components are used for components that need to manage state or have lifecycle methods.

# State in React:
- In React, state is used to manage the internal data of a component. 
- It is an object that stores the data that can change within a component. 
- When the state of a component changes, React will re-render the component with the updated data. 
- State can only be modified within the component where it is defined and cannot be accessed or modified by any other component. 
- The state can be initialized in the constructor of a component, and it can be updated using the setState() method.

# Props in React:
- In React, props (short form for "properties") are used to pass data from a parent component to a child component. 
- Props are read-only, and a child component cannot modify the props it receives from its parent. 
- Props are passed to a component as attributes, and they are accessed using the "this.props" keyword.

# Controlled Components:
- In React, the Controlled Component pattern involves managing the component’s state through React’s state system. The component’s state is controlled and updated by React, and changes are reflected through props.
- This pattern allows for a more predictable and controlled flow of data in the application.

# What is a higher order component?
- A Higher-Order Component (HOC) in React is a function that takes a component and returns a new component with added functionality. HOCs are used for reusing component logic and abstracting common behaviors.

# When rendering a list what is a key and what is it's purpose?
- Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys. When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort. It is not recommend to use indexes for keys if the items can reorder, as that would be slow.

# What are refs used for in React?
- In React, refs are used to access DOM elements or React elements directly. Here are some common use cases for refs in React:
1. Accessing DOM Elements: You can use refs to get a reference to a DOM element and directly manipulate it. This is useful for focusing on input fields, playing media, or getting the value of an element.
2. Managing Focus: You can set the focus to a specific element, such as an input field.
3. Triggering Animations: refs can be used to directly access and manipulate elements to trigger animations or transitions.
4. Storing Instance Variables: You can use refs to store any mutable value that doesn't cause a re-render when changed. This is often used to store instance variables in functional components.
5. Integrating with Third-Party Libraries.

# What is redux?
- Redux is a state management library for JavaScript applications, most commonly used with React.
- The basic idea of redux is that the entire application state is kept in a single store. The store is simply a javascript object. (The entire state of your application is stored in a single JavaScript object called the store.)
- The only way to change the state is to dispatch an action, which is a plain JavaScript object describing what happened. and then writing reducers for these actions that modify the state.
# Difference between action and reducer.
- Action:--
 - Actions are plain javascript objects.
 - They must have a type indicating the type of action being performed.
 - In essence, actions are payloads of information that send data from your application to your store.
- Reducer:--
 - A reducer is simply a pure function that takes the previous state and an action, and returns the next state.
# What is  Redux Thunk used for?
    -  Redux Thunk is middleware that allows you to write action creators that return a function instead of an action.
# What is the useEffect hook used for?
    - The useEffect hook is used for performing side effects in functional components. This can include things like data fetching, setting up subscriptions, manually changing the DOM, setting up timers. The useEffect hook is called after the component renders, and can be used to ensure that your component stays up-to-date with any relevant data or dependencies.

# Why virtual DOM is faster to update than real DOM?
    - The virtual DOM is faster to update than the real DOM because  React uses a clever technique to minimize the number of updates that need to be made to the real DOM.
    - When you update the virtual DOM,  React will compare the new virtual DOM with the old one, determine which parts have changed, and then update the real DOM accordingly. This means that only the parts of the DOM that actually need to be changed are updated, which is much faster than updating the entire DOM every time there is a change.
# What are some common hooks that are used in React?
    - Some common hooks that are used in React include useState, useEffect, and useContext. 
    - The useState hook allows a functional component to have local state, 
    - The useEffect hook allows a functional component to perform side effects, 
    - The useContext hook allows a functional component to access values from the nearest context provider.
# React Router / types of routers 
    - React Router is a standard library for routing in React applications. It enables the navigation between different components in a React application, changing the browser URL, and keeping the UI in sync with the URL.
# What is Lifting State Up in React?
    - When several components need to share the same changing data then it is recommended to lift the shared state up to their closest common ancestor. That means if two child components share the same data from its parent, then move the state to parent instead of maintaining local state in both of the child components.
#  What is children prop?
    - Children is a prop that allows you to pass components as data to other components, just like any other prop you use. Component tree put between component's opening and closing tag will be passed to that component as children prop.
# useMemo Hook - 
    -useMemo is used to sapplay memoization in react.
    -memoization is a technique for improve the performance of the code.
    - it is useful to avoid expensive calculations on every render when the returned value is not changed.
    - we can stop running unwanted functions on re-rendering
# difference between useEffect and useMemo?
    - syntax are similar
    - in useEffect hook we can't return value and can't store in a variable, but in useMemo we can return value and store in a variable.
# custom hook
    - custom hooks are basically a reusable function.
    - custom hooks are your logic which you created as a reusable function.
    - you can use multiple hooks and create something that will help you to skip repeated tasks in your project.
# JavaScript questions =>
 https://chatgpt.com/share/ef7ce897-f4b6-49f0-8521-3bced63af3f5

# Event Loop:

The event loop is a fundamental concept in JavaScript that handles asynchronous operations and ensures non-blocking execution. It allows JavaScript to perform long-running operations without freezing the entire program. Here's a breakdown of how the event loop works:
 
### 1. Single-Threaded Nature of JavaScript
JavaScript is single-threaded, meaning it has a single call stack, and it can do one thing at a time. This can be problematic for long-running tasks, but the event loop helps manage these tasks efficiently.
 
### 2. Call Stack
The call stack is a data structure that keeps track of function calls. When a function is called, it’s added to the stack, and when it returns, it’s removed from the stack.
 
### 3. Web APIs
Web APIs are provided by the browser (or Node.js in the case of server-side JavaScript) to handle asynchronous operations such as DOM events, HTTP requests, and timers. These operations do not run on the main call stack but are instead handled by the browser or Node.js environment.
 
### 4. Task Queue (Callback Queue)
When an asynchronous operation completes, its callback function is moved to the task queue. This queue stores all the callback functions that are ready to run.
 
### 5. Event Loop
The event loop continuously checks if the call stack is empty. If it is, it takes the first callback from the task queue and pushes it onto the call stack, effectively allowing it to execute.
 
### 6. Microtask Queue
In addition to the task queue, there’s a microtask queue that handles promises and other microtasks. The event loop gives priority to the microtask queue, ensuring that all microtasks are executed before moving on to the task queue.
 
### Example
 
Here's an example to illustrate the event loop:
 
javascript
console.log('Start');
 
setTimeout(() => {
  console.log('Timeout');
}, 0);
 
Promise.resolve()
  .then(() => {
    console.log('Promise');
  });
 
console.log('End');

 
### Execution Steps:
 
1. **Call Stack**: The call stack starts with the `console.log('Start')` call.
   - Output: `Start`
   - Call Stack: `console.log('Start')`
 
2. **Call Stack**: The `setTimeout` call is encountered. The callback function is registered and moved to the task queue.
   - Output: `Start`
   - Call Stack: `setTimeout(callback, 0)`
 
3. **Call Stack**: The `Promise.resolve().then(...)` call is encountered. The callback is registered and moved to the microtask queue.
   - Output: `Start`
   - Call Stack: `Promise.then(callback)`
 
4. **Call Stack**: The `console.log('End')` call is executed.
   - Output: `Start`, `End`
   - Call Stack: `console.log('End')`
 
5. **Microtask Queue**: The microtask queue is checked next. The promise callback is executed.
   - Output: `Start`, `End`, `Promise`
   - Call Stack: `Promise.then(callback)`
 
6. **Task Queue**: The task queue is checked next. The `setTimeout` callback is executed.
   - Output: `Start`, `End`, `Promise`, `Timeout`
   - Call Stack: `setTimeout(callback)`
 
### Summary
The event loop ensures that JavaScript remains non-blocking and efficient, even with asynchronous operations. By managing the execution of callbacks in a well-defined order, the event loop allows for smooth, responsive applications.