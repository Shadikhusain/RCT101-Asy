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


