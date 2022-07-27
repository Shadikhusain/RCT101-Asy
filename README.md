## Day1 RCT101 Theory quetn.

1. What is React?
  ANS:- React is a free and open-source front-end JavaScript library for building user interfaces based on UI components. It is maintained by Meta and a community of individual developers and companies.
  
2.Who made React?
ANS:-React was originally created by Jordan Walke. Today, React has over a thousand open source contributors. We'd like to recognize a few people who have made significant contributions to React and its documentation in the past and have helped maintain them over the years: This list is not exhaustive.

3.What is Babel?
ANS:-Babel is a free and open-source JavaScript transcompiler that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript that can be run by older JavaScript engines. Babel is a popular tool for using the newest features of the JavaScript programming language. 

4.How does Babel convert html code in React into valid code?
ANS:-Browsers don’t understand JSX out of the box, so most React users rely on a compiler like Babel or TypeScript to transform JSX code into regular JavaScript. Many preconfigured toolkits like Create React App or Next.js also include a JSX transform under the hood.

Together with the React 17 release, we’ve wanted to make a few improvements to the JSX transform, but we didn’t want to break existing setups. This is why we worked with Babel to offer a new, rewritten version of the JSX transform for people who would like to upgrade.
Code:
import React from 'react';
function App() {
  return <h1>Hello World</h1>;
}
import React from 'react';

function App() {
  return React.createElement('h1', null, 'Hello world');
}

5.What is ReactDOM used for? Write an example?
The react-dom package provides DOM-specific methods that can be used at the top level of your app and as an escape hatch to get outside the React model if you need to.
EX:
import * as ReactDOM from 'react-dom';
var ReactDOM = require('react-dom');
createPortal(child, container)
flushSync(callback)
// Force this state update to be synchronous.
flushSync(() => {
  setCount(count + 1);
});
// By this point, DOM is updated.
render()
render(element, container[, callback])
hydrate()
hydrate(element, container[, callback])

6.What are the packages that you need to import for react to work with?
ANS:-I was trying to wrap material-ui components like iconButton, iconMenu, etc. to make the components easy to use programatically. To put them into a git repository I need a example directory with a seperate react project using the components I developed. So, I need to develop a package that hold components' definitions and exporting them to be used in other project. I want to keep my implementations private so I cannot even publish it to npm.js.

[you can see the question statement for thorough understanding of thr ptoblem.]

Coming to the solution help me doing the needed, I created a new project with yarn adding minimal dependencies. i.e.

babel
babel-cli
babel-core
babel-loader
babel-preset-es2015
babel-preset-react
babel-preset-stage-2
html-webpack-plugin
raw-loader
webpack
webpack-dev-server
and then devDependencies

react
react-dom

7.How do you add react to a web application?
ANS:-React has been designed from the start for gradual adoption, and you can use as little or as much React as you need. Perhaps you only want to add some “sprinkles of interactivity” to an existing page. React components are a great way to do that.

The majority of websites aren’t, and don’t need to be, single-page apps. With a few lines of code and no build tooling, try React in a small part of your website. You can then either gradually expand its presence, or keep it contained to a few dynamic widgets.

Add React in One Minute
Optional: Try React with JSX (no bundler necessary!)
Step 1: Add a DOM Container to the HTML
First, open the HTML page you want to edit. Add an empty <div> tag to mark the spot where you want to display something with React. For example:

<!-- ... existing HTML ... -->

<div id="like_button_container"></div>

<!-- ... existing HTML ... -->
We gave this <div> a unique id HTML attribute. This will allow us to find it from the JavaScript code later and display a React component inside of it.

Tip

You can place a “container” <div> like this anywhere inside the <body> tag. You may have as many independent DOM containers on one page as you need. They are usually empty — React will replace any existing content inside DOM containers.

Step 2: Add the Script Tags
Next, add three <script> tags to the HTML page right before the closing </body> tag:

  <!-- ... other HTML ... -->

  <!-- Load React. -->
  <!-- Note: when deploying, replace "development.js" with "production.min.js". -->
  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

  <!-- Load our React component. -->
  <script src="like_button.js"></script>

</body>
The first two tags load React. The third one will load your component code.

Step 3: Create a React Component
Create a file called like_button.js next to your HTML page.

Open this starter code and paste it into the file you created.

Tip

This code defines a React component called LikeButton. Don’t worry if you don’t understand it yet — we’ll cover the building blocks of React later in our hands-on tutorial and main concepts guide. For now, let’s just get it showing on the screen!

After the starter code, add three lines to the bottom of like_button.js:

// ... the starter code you pasted ...

const domContainer = document.querySelector('#like_button_container');
const root = ReactDOM.createRoot(domContainer);
root.render(e(LikeButton));

8.What is React.createElement?
ANS:-React. createElement( type, [props], [... children] ) Create and return a new React element of the given type. The type argument can be either a tag name string (such as 'div' or 'span' ), a React component type (a class or a function), or a React fragment type.

9.What are the three properties that createElement accept?

The createElement() method creates an element node. See Also: The Element appendChild() Method · The Element insertBefore() Method. Syntax.  

<!DOCTYPE html>
<html>
<body>

<h1>The Document Object</h1>
<h2>The createElement() Method</h2>

<p>Create a p element with some text:</p>

<script>
// Create element:
const para = document.createElement("p");
para.innerText = "This is a paragraph.";

// Append to body:
document.body.appendChild(para);
</script>

</body>
</html>


10. Render:-Render is a synonym of make — technically it means "cause to become." An illness might render you unable to walk, or a shocking sight might render you speechless.

Another basic meaning of the verb render is to give, present, or perform something: you could render assistance to someone in need, for example. And a specialized sense is to formally declare a verdict in a court case. Render derives from the Latin verb reddere, "to restore," from the prefix re-, "back," plus dare, "to give."

Root:-The root element is the root element of the React DOM tree. It's the element passed to the rendering function ReactDOM.render. Articles Related App In a app.
