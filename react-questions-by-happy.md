1. what are the react component? what are the main elements of it?
2. what is SPA?
3. Advantages/Disadvantages of React
4. role of JSX
5. diff between imperative and declarative syntax
6. What is arrow function expression in jsx
7. how to setup React first project?
8. what are the main files in react project?
9. How react app load and display the components in browser?
10. what is diff bet react and angular?
11. what are other 5 js frameworks other than react?
12. whether react is a framework or library? what is the diffeence?
13. How react provides reusability and composition?
14. what are state, Stateless, Stateful and State Management terms?
15. what are props in jsx
16. what is npm? what is the role of node_modules folder?
17. what is the role of public folder in react?
18. what is the role of src folder in react?
18. what is the role of index.html page in react?
18. what is the role of index.js file and ReactDOM in react?
18. what is the role of App.js file in react?
18. what is the role of function and return inside App.js?
19. can we have a function without a return inside App.js?
20. What is role of export default inside App.js?
21. does the file name and the component name must be same in react?

## JSX

1. what is the role of jsx 
2. advantage of jsx
3. what is babel
4. what is role of fragement in react
5. what is spread operator in jsx?
6. what are types of conditional rendering in react js?
7. How do you iterate over a list in jsx? what is map()?
8. can browser read a jsx file?
8. what is transpiler and diff bet transpiler and compiler?
9. is it possible to use jsx without react?
=> yes.

## components functional/ class
1. what are the react components? what are the main elements of it?
2. what are types of react components? what is functional component?
3. how do you pass data in functional components?
4. what is prop drilling in react?
5. why to avoid prop drilling? in how many ways can avoid prop drilling?
6. what are class component?
7. how to pass data between class component?
8. what is role of this keyword in class component
9. diff bet class and functional component


## Routing
1. what is routing and router in react? 
2. how to implement routing in react
3. what are the roles of <Route> and <Routes> component in react routing?
4. what are Route Parameters in react routing?
5. what is the role of Switch component in react route
=> Switch component ensures that the only first matching <Route> is rendred and rest are ignored.
6. what is the role of exact prop in react routing?

## Hooks - useState/ useEffect
1. what are react hooks? what are the top react hooks?
2. what are state, stateless, statefull and state management terms?
3. what is role of useState() hook and how it works?
4. what is role of useEffect() hook and how it works and what is its use?
5. what is Dependency Array in useEffect() hook?
6. what is the meaning of the empty array [] in useEffect?

## Hooks - useContext/ useReducer
1. what is the role of usereducer hook?
2. what is createContext()? what are provider and consumer properties?
3. when to use useContext() hook instead of props in real application?
4. what is the similarities between usState() and useReducer()?
5. what is useReducer hook? when to use useState() and usereducer()?
6. what is the diff bet useState() and useReducer() hook?
7. what are dispatch and reducer function in useReducer hook?
8. what is the purpose of passing initial state as an object in UseReducer?

## component lifecycle methods - 1
1. what are component life cycle phase?
=> 1. Mounting Phase - component creation started
    - This phase occurs when an instance of a component is being created and inserted into the DOM.

    2. Updating phase - compoenent updates
     - This phase occurs when a component is being re-rendered as a result of changes to either its props or state.

    3. unmounting phase - removal from DOM
    - this phase occurs when a component is being removed from the DOM.

2. what are component life cycle methods?
    * Mounting Pahse - methods are given below
        1. Constructor()
        2. getDerivedStateFromProps()
        3. render()
        4. componentDidMount()
    * Updating phase - methods are given below
        1. getDerivedStateFromProps()
        2. shouldComponentUpdate()
        3. render()
        4. getSnapshotBeforeUpdate()
        5. componentDidUpdate()
    * Unmunting pahse - 
        1. componentWillUnmount()


3. what are constructor in class components? when to use them?
4. what is the role of super keyword in constructor?
5. what is the role of render() method in component life cycle?
6. How the State can be maintained in a class component?
7. what is the role of componentDidMount() method in component life cycle?

## Controlled and uncontrolled components

1. what are controlled component in react?
    - a controlled component is a component whose form elements like input fields or checkboxes are controlled by the state of the application.

2. Diff between controlled and uncontrolled component?

    * Controlled Components- 
        1. values are controlled by React State.
        2. Event handlers update react state.
        3. Don't depend on useRef().
        4. re-render in state changes.
        5. a recommended and standard practice for form handling in react.

    * uncontrolled Component- 
        1. values are not controlled by React State. 
        2. no expicit state update; values can be accessed directly from the DOM.
        3. Commenly uses useRef() to access form element values.
        4. less re-rendering since values are not directly tied to react state.
        5. useful in certain scenarios but less commonely considered a best practice.

3. what are characteristics of controlled component?
    - State Control-
    - Event Handling-
    - State update - 
    - re-rendering

4. what are the addvantages of using controlled components in react forms?

5. how to handle forms in react?
    - The preferred and recommended approach for handeling forms in react is by using controlled components.

6. how can you handle multiple input fields in a controlled form?
    - maintain separate state variables for each input field and update them individually using the onChange event.

7. how do you handle form validatioan in a controlled compoenent?
8. in what scenarios might using uncontrolled components be advantageous?

## Code splitting

1. what is code spliting in react?
    - code splitting is a technique to split the javascript bundle into smaller chunks, which are loaded on demand.

2. how to implement code splitting in react?
    - 3 steps for code spitting in react
    1. Use React.lazy() to lazily import component.
    2. wrap components with Suspense to handle loading.
    3. configure your build tool(e.g. webpack) for dynamic imports.

3. what is the role of Lazy and Suspense method in React?

    - In React, React.lazy and Suspense are used to improve the performance of your application by enabling code-splitting and lazy loading of components. This allows you to load components only when they are needed, rather than loading everything upfront. Here's an overview and a basic example of how to use them:

    1. React.lazy
        React.lazy allows you to dynamically import a component, which means that the component will only be loaded when it's actually needed.

    2. Suspense
        Suspense is a component that allows you to specify a fallback UI (like a loading spinner) that is shown while your lazy-loaded component is being loaded.

4. what are the Prons and Cons of code Splitting?
5. what is the role of the import() function in code splitting?
6. what is the purpose of the fallback prop in Suspense?
7. can you dynamically load css files using code splitting in react?
8. How do you inspect and analyze the generated chunks in a react application? 


 