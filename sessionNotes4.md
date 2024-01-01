E1 P4 - TOPICS

- Does the order of the file matter?
- what is root.render(parent) doing?
- what will happen if my root has already something else?
- What is react - library or a framework?

- ? IMP - Does the order of the file matter or not?

Yes, it does matter

<script src="./App.js"></script>

If we move this above the two files of react it will throw an error as "React is not defined"

<script src="./App.js"></script>
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

This is because App.js is using the above two files

- ? what is root.render(parent) doing?
  It is basically putting the parent inside the root tag( inside the HTML file)

- ? what will happen if my root has already something else?

 <div id="root">
    <h1>Someone else was here!</h1>
 </div>

If something is inside the HTML file already i.e the root of the div tag, this will get replaced by:

- root.render(parent);

First it will it will load whatever is the root of the HTML and print it.
Then it loads the react scripts
Next it loads the App.js file and reads the code line by line
The minute it loads the root.render it replaces everything in the root with the parent.

- REACT works only inside ROOT
- React REPLACES and not APPENDS inside the root
- Everything renders inside the root element
- This is why React is called a Library and not a framework
- React can be applied to small portion of our page itself (header, footer, sidebar) -> whatever we make the root as!

If we give anything before or after root it will be printed just like that

Advantages

- Not all frameworks can be applied to other apps
