E1 P2 - TOPICS

- What are the two files injected in our code?
- Why do we use 2 files?
- How do we create a h1 using react?
- What is React.createElement?

- React is a Javascript Library - (Is just Javascript files)

If we type React in our console, we get the below in our console.
{Children: {…}, Fragment: Symbol(react.fragment), Profiler: Symbol(react.profiler), Component: ƒ, PureComponent: ƒ, …}

You will also able to see the below:
\_\_SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED
:
{ReactCurrentDispatcher: {…}, ReactCurrentOwner: {…}, ReactCurrentBatchConfig: {…}, Scheduler: {…}, ReactCurrentActQueue: {…}, …}

- Why there are two files?
  React doesnt work only on browsers, it also works on mobiles (React Native), React 3D.
  There are different functions used in different environments.

File 1 (react.development.js) - This is the core of React
File 2 (react-dom.development.js) - This is useful for DOM operations
-> More like a bridge to connect react to the browsers

 <script>
    // Creating a h1 tag using react
    React.createElement()
    This takes three arguments:
    1. What Tag ("h1")
    2. Object ({}) // Empty object for now
    3. What needs to be put inside the tag/ children ("Hello World from React!");

    React.createElement("h1",{},"Hello World from React!");

** We first need to tell React what is the root where we need to render it! **
** React needs to have a Root to do DOM manipulation



</script>

createElement -> Core thing of React which comes from the react-developement.js file
creating a root and rendering something inside it is the job of react-dom.developement.js

<script>
     const heading = React.createElement("h1",{},"Hello World from React!");
     const root = ReactDOM.createRoot(document.getElementById("root"));
     // whatever we render we can do this in our header
     root.render(heading);
</script>

Everything runs inside the root
React.createElement, ReactDOM, root.render => all these are putting the heading inside our root
