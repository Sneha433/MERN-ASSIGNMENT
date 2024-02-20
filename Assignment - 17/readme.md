# DAY 01 - REACT ASSIGNMENT

## Theory
- **What is Emmet?**
- It is a plugin or developer tool kit that helps make work faster and substantially enhances HTML and CSS workflows
   eg html:5
      link:css
  
- **Difference between a Library and Framework?**
- Library:
    library is like a chocolate which is simple doesn't provide structure for developers to build.
    It can reusable the code. 
Framework:
    Framework is like Military ,they provide structure for developers to build.
    It cannot reuseable the code.
  
- **What is CDN? Why do we use it?**
- CDN(content delivery network)-Faster Load Times,CDN servers are optimized for quick content delivery, reducing the time it takes for web pages to load.
- 
- **Why is React known as React?**
- It "reacts" quickly to changes without reloading the whole page.
- 
- **What is crossorigin in the script tag?**
- The crossorigin attribute sets the mode of the request to an HTTP CORS Request And It also overcome CORS ERROR.

- **What is the difference between React and ReactDOM?**
- React provides the tools and concepts to define component-based user interfaces.ReactDOM handles the task of rendering those interfaces in a web environment. 
   
- **What is the difference between react.development.js and react.production.js files via CDN?**
- React. js builds your project in development mode, which includes features like detailed error messages and debugging tools
   it's important to build it in production mode to benefit from optimized performance and reduced bundle size.

- **What is async and defer?**
-  async and defer both load JavaScript asynchronously without render blocking, but async executes as soon as possible and in no particular order while defer runs in sequence toward the end of the loading process, just before the DOMContentLoaded event.


## Coding
### Set Up Tools
- Install the following tools on your laptop:
  - [VS Code](https://code.visualstudio.com/)✅
  - [Chrome](https://www.google.com/chrome/)✅
  - Install relevant extensions for Chrome✅

### Create a New Git Repo
- Initialize a new Git repository.✅

### Build Your First Hello World Program
1. **Using Just HTML**
2. **Using JS to Manipulate the DOM**
3. **Using React**
   - Use CDN Links
   - Create an Element
    ```jsx  
      <h1 class="heading">Heading</h1>
    ```
   - Create Nested React Elements
   ```jsx  
     <div id="1">
       <div id="2">
         <h1 class="heading">Heading</h1>
         <h1 class="heading">Heading</h1>
       </div>
     </div>
     ```
   - Use `root.render`

### Push Code to GitHub
- Push both theory and code to your GitHub repository.

### Learn About Arrow Functions
- Familiarize yourself with Arrow Functions

 <!--html code-->
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React-1</title>
    <link rel="stylesheet" href="./style.css"> 
</head>
<body>

  <!--<h1 id="headingElement"></h1>-->
  <div id ="content">
       <p>sneha</p>
  </div>

  <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
 
<script src = "./script.js"></script>  
</body>
</html>

<!--css code-->
.heading{
    color: rgb(143, 42, 190);
}

<!-- js code-->
//const headingElement = document.getElementById("headingElement")
// headingElement.textContent="Hello World"
//---create an element----
const headingElement = React.createElement(
    "h1",{"class":"heading"},
    "Hello World"
);
//---nested react element---
const reactElement = React.createElement(
    "div",
    {id:"1"},
  React.createElement("div",{id:"2"},[
    React.createElement("h1",{class:"heading"},"Heading"),
    React.createElement("h1",{class:"heading"},"Heading"),
  ])
);

const root = ReactDOM.createRoot(document.getElementById("content"));//<div id ="content"> </div>
console.log(root);
// convert the obj and replaced to HTML DOM
//root.render(headingElement);
root.render(reactElement);
 // output = hello World
  
