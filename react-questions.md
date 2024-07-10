# How does react works?
React creates a virtual DOM. When a state chages in a component, it first runs a "diffing" algorithm which identifes what has changed in Virtual DOM. The second step is reconciliation, where it updates the dom with the result of diff.

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
    These are simple JavaScript functions that take props as input and return JSX elements. They are often used for presentational or stateless components.

# Class Components:
    These are ES6 classes that extend from React.Component or React.PureComponent. They have a render() method where you define the structure of your component's UI using JSX. Class components are used for components that need to manage state or have lifecycle methods.

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

# When rendering a list what is a key and what is it's purpose?
- Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys. When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort. It is not recommend to use indexes for keys if the items can reorder, as that would be slow.