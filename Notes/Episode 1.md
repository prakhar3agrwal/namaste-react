Episode 1, Part 1:
VS code uses Emmet - generates code
What is CrossOrigin?

2 files from CDN
1. Development contains the core logic as react runs on mobile, 3D etc and not only on browsers.
2. react-DOM to deal with DOM, browser specific. Bridge between browser and react

Episode 1, Part 2:

React needs a root where all the DOM related stuff can be done by it. This is the root. ReactDOM.createRoot

React.createElement is a core function for creation of an element and hence present inside React but createRoot is related to DOM and when we 
need to put it in browser we create a root, hence present in ReactDOM.

The most expensive operation in a web page is when we do something on UI and the DOM nodes/tree needs to be manipulated. All the frameworks try to optimize it. React was build with a philiosophy that we want to manipulate our DOM with Javascript.



React.createElement("h1", {}, "Hello World from React") - The second argument is used to provide attributes to the tag, eg id, class etc
The above function returns a react element which is basically a JS object.
It contains an atrribute names props which contains children  and other stuff. The 3rd arg/content is the children and others are attributes. (children + attributes)
The render method takes this react element and converts it into H1 tag to show on UI.
 -----------------------------------------------------------------------------------
<div>

    <div>
        <h1>Hello World from React</h1>
    <div>
<div>

const parent =  React.createElement("div", {id: "parent"}, 
    React.createElement("div", {id:"child"}, 
        React.createElement("h1", {}, "Hello World from React")));


ReactElement(Object) => HTML (Browser inderstands)
-------------------------------------------------------------------------------------


<div>

    <div>
        <h1>I am H1 tag</h1>
        <h2>I am H2 tag</h2>
    <div>
<div>

const parent =  React.createElement("div", {id: "parent"}, 
    React.createElement("div", {id:"child"}, 
        [React.createElement("h1", {}, "I am H1 tag"),React.createElement("h2", {}, "I am H2 tag")]));

If we want to pass siblings, we can pass it in the form of an array.


This code looks ugly and will be fixed via JSX.

Episode 1, Part 5:

If we already have something inside the root, then it will be replaced(not appended) by the content passed through root.render()
React is a library(not a large framework), can work in a very small part of our app as well. It only works on the root that we have specified. Other parts remain as it is.

Order of files also matter, cant use react before loading it from CDN.
