# How does react works?
React creates a virtual DOM. When a state chages in a component, it first runs a "diffing" algorithm which identifes what has changed in Virtual DOM. The second step is reconciliation, where it updates the dom with the result of diff.

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