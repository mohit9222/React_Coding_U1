/** Inception **/

E1 P1 - TOPICS

- Emmet
- Writing hello world using HTML
  - Writing hello world using Javascript
  - CDN
- First way to add react to our code - Using CDN

VS Code uses something called as EMMET
Emmet - Used to generate code is VS code
Ex: html:5 + enter

We will get the following HTML code structure automatically

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React</title>
</head>
<body>
    
</body>
</html>

We are creating a basic hello world! in html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React</title>
</head>
<body>
     <!--We are creating a root container -->
    <div id="root">
        <!-- Creating Heading -->
        <h1>Hello World!</h1>
    </div>
</body>
</html>

Creating our Hello world but using Javascript

We need to add heading using Javascript
To add JS in our page we use <script> tag

we make use of the document.createElement() API

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React</title>
</head>
<body>
     <!--We are creating a root container -->
    <div id="root">
        <script>
            const heading = document.createElement("h1");
            heading.innerHTML = "Hello Word from Javascript!";
            const root = document.getElementById("root"); 
            root.appendChild(heading);
            // First we need to find our root 
            // This root gets reference to this <div> tag on line 10
            // This is there on every HTML node
            // This heading will go inside this root as a child
        </script>
    </div>
</body>
</html>

Creating our Hello world but using React JS

- Browser doesnt know or doesnt understand what is React code
- Our project right now is not configured to use React
- We need to add React in our code

First way to add React into our code is via CDN (Content Delivery Network)
_CDN_ -> Place where the react library is hosted

- What is CDN?
- Why do we use CDN?

With the help of these CDN links we have injected React in our code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React</title>
</head>
<body>
     <!--We are creating a root container -->
    <div id="root">
        <!-- With the help of these CDN links we have injected React in our code -->
        <script 
            crossorigin src="https://unpkg.com/react@18/umd/react.development.js">
        </script> // link where react code is hosted
        <script 
            crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js">
        </script>
    </div>
</body>
</html>
