E1 P3 - TOPICS

- Good practices to be followed
- Most expensive thing for a browser
- what is empty object in createElement?
- Adding a css file to our app
- React Element
- Props
- How do we create the HTML structure in React?
- How do we add sibilings to it

- Good practice:
Move all our react code to a seperate Javascript file
Moving all the react code to App.js
We need to inject our react code inside our App.js file
<script src="./App.js"></script>

- The most expensive (costly operation) thing for a browser is manipulating DOM(tree)
  - Things that need to be added or delated
  - Every framework or library AIMs to do this in a very efficient way and optimise this.

const heading = React.createElement("h1",{},"Hello World from React!");
{} -> Is the place where we will give attributes to our tags

const heading = React.createElement(
"h1",
{id: "heading"},
"Hello World from React!"
);

If you check your console, you will see the following:

<div id="root">
    <h1 id="heading">Hello World from React!</h1>
</div>

we can add a css file to our app

<link rel="stylesheet" href="./index.css" />

coloring our heading id (attributes)

- what is React.createElement("h1",{},"Hello World from React!"); or what is this heading?
  If we console this heading we will get a object which is a react element

React element - Is nothing but a normal JS object
props - children + attributes we pass
{id: "heading"}, - > attributes
"Hello World from React!" - > children goes inside h1 tag

root.render(heading) - we are passing a react element to it
The job of root.render is to take the object, create a h1 tag(that browser understands) and put it inside the root element

Our HTML structure is generally structured (nested way)

<div id="parent">
    <div id="child">
        <h1>I am H1 Tag</h1>
    </div>
</div>

How do we create the above structure in React?

<script>
const parent = React.createElement(
    "div",{id: "parent",
     React.createElement(
        "div",{id: "child",
            React.createElement(
                "h1",
                {},
                "I am a H1 Tag"
            )
        })
    })
</script>

- React.createElement (object) => HTML (Browser Understands)

How do we add siblings to the h1 tag, adding a h2 tag within the same structure?

<div id="parent">
    <div id="child">
        <h1>I am H1 Tag</h1>
        <h2>I am H2 Tag</h2>
    </div>
</div>

- We make use of an "ARRAY"/ We need to convert the third argument into an array
<script>
const parent = React.createElement(
    "div",{id: "parent",
     React.createElement(
        "div",{id: "child",
            React.createElement(
                [
                    React.createElement(
                        "h1",
                        {},
                        "I am a H1 Tag"
                    ),
                    React.createElement(
                        "h2",
                        {},
                        "I am a H2 Tag"
                    ),
                ]
            )
        })
    })
</script>

How do we add two children within the same structure?

<div id="parent">
    <div id="child1">
        <h1>I am H1 Tag</h1>
        <h2>I am H2 Tag</h2>
    </div>
    <div id="child2">
        <h1>I am H1 Tag</h1>
        <h2>I am H2 Tag</h2>
    </div>
</div>

Same way by using the Array

<script>
const parent = React.createElement("div", { id: "parent" }, [
  React.createElement("div", { id: "child1" }, [
    React.createElement("h1", {}, "I am a H1 Tag"),
    React.createElement("h2", {}, "I am a H2 Tag"),
  ]),
  React.createElement("div", { id: "child2" }, [
    React.createElement("h1", {}, "I am a H1 Tag"),
    React.createElement("h2", {}, "I am a H2 Tag"),
  ]),
]);
</script>

This makes the code unmaintainable and unreadable.
This is why we have something called as JSX(Javascript XML)
All the above code is of React 18
