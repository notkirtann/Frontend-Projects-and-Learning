# Coffee Aur React - Hitesh Choudhary  Notes
## Introduction to React
- React is a JavaScript library for building user interfaces.
- It allows developers to create large web applications that can update and render efficiently in response to data changes.
- React follows a component-based architecture, where the UI is divided into reusable components.
- It uses a virtual DOM to optimize rendering and improve performance.

### Difference between library and framework
- A library is a collection of pre-written code that developers can use to optimize tasks. It provides specific functionality and allows developers to call its functions as needed. React is an example of a library because it focuses on building user interfaces and can be integrated into various projects without enforcing a specific structure.
- A framework, on the other hand, is a more comprehensive solution that provides a foundation for building applications. It often dictates the architecture and structure of the application, providing a set of rules and guidelines for development. Frameworks typically include libraries, tools, and best practices to streamline the development process. Examples of frameworks include Angular and Vue.js.
In summary, a library offers specific functionality that can be used as needed, while a framework provides a complete structure and set of guidelines for building applications.


## Key Concepts
1. **Components**: The building blocks of a React application. They can be functional or class-based.
2. **JSX**: A syntax extension for JavaScript that allows you to write HTML-like code within JavaScript.
3. **Props**: Short for properties, props are used to pass data from parent to child components.
4. **State**: A built-in object that allows components to manage and respond to data changes.
5. **Lifecycle Methods**: Special methods in class components that allow you to hook into different stages of a component's lifecycle (e.g., mounting, updating, unmounting).
6. **Hooks**: Functions that let you use state and other React features in functional components (e.g., useState, useEffect).


## Setting Up a React Project
create-react-app is a popular tool to set up a React project quickly.
```bash 
npx create-react-app my-app
cd my-app
npm start
``` 
This will create a new React project and start a development server.
using Vite
```bash 
npm create vite@latest my-react-app -- --template react
cd my-react-app 
npm install
npm run dev
```
This will create a new React project using Vite and start a development server.
why vite?
- Faster development server startup times
- Improved build performance
- Enhanced support for modern JavaScript features
- Built-in support for TypeScript and JSX
- Simpler configuration compared to traditional bundlers like Webpack

### Difference between Vite and Create React App
- Vite is a modern build tool that leverages native ES modules and provides faster development experiences, while Create React App is a more traditional setup that uses Webpack under the hood.
- Vite offers instant server start and lightning-fast hot module replacement (HMR), whereas Create React App may have slower startup times and HMR performance.

## Creating a Simple Component
```jsx
import React from 'react';
function HelloWorld() {
  return <h1>Hello, World!</h1>;
}
export default HelloWorld;
```
This is a simple functional component that renders "Hello, World!" to the screen.
## Rendering Components
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import HelloWorld from './HelloWorld';
ReactDOM.render(<HelloWorld />, document.getElementById('root'));
```
This code renders the `HelloWorld` component into the DOM element with the ID of `root`.
## Conclusion
React is a powerful library for building user interfaces with a component-based approach. By understanding its key concepts and setting up a project, you can start building dynamic web applications efficiently.




