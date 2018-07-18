# reactStarters

## First things first.
### What does ReactDOM.render do?  
Signature --  
```js
ReactDOM.render(whatToRender, whereToRender)
```  
It accepts 2 arguments.  
1. what to render -- an html element or a react component  
2. where to render -- in your base html, where to put the above component. It should have a home to stay afterall!  
This basically means, you must have a div or something of that sort which can provide place for the component you've created or just any html to stay in.  
**A generous div that can hold the component or html you created dearly!**   
Well, we can locate it by id or querySelector or whatever!  

Example:  
```html
<html>
    <head>
       <title>Hello React</title>
    </head>
    <body>
        <div id="root-container"></div>

        <!-- Load React. -->
        <script src="https://unpkg.com/react@16/umd/react.development.js" crossorigin></script>
        <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js" crossorigin></script>

        <!-- Load our React component. -->
        <script src="helloReact.js"></script>
    </body>
</html>
```
Here, 
```html
<div id="root-container"></div>
```
is our generous, great div! :P

### What does React.createElement do?
Signature -- 
```js 
React.createElement(component, props, ...children) 
```
It accepts 3 arguments.  
1. component -- think of it as an html tag (Maybe a div or h1 or anthing else to start with)
2. props -- these are like attributes to html tag. If there are no props, this arg is set to null.
> Example: Let's say,   
```html 
<div someAttrib = "abcd">Hey there!</div>
```  
is the component/html we want to display/render on the screen (I know, this someAttrib prop makes no sense here. But bear with me here). Here someAttrib is a prop in React world :P
So, createElement call will look like:
```js
React.createElement('div', {someAttrib:"abcd"}, "Hey there!") 
```
3. ...children  
[... is spread operator.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)  
Oh, don't worry abt it right now!  
Content that comes inside the html tag / the component comes here.
In the above example, "Hey there!" is the child.  
> FYI: it can have expressions too.. We'll come to it later!
