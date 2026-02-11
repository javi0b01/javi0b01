# :memo: Notes
## REACT
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [React](https://react.dev/)
- [ViteJS](https://vitejs.dev/)
- [Create React App](https://create-react-app.dev/)
- [React Bootstrap](https://react-bootstrap.github.io/)
- [styled-components](https://styled-components.com/)
- [MATERIAL-UI](https://material-ui.com/)
* Extension
  - react developer tools
- [Training React](https://github.com/javi0b01/training-react)
### Requirements
- Nodejs
### Setup
#### Vite
```
$ npm create vite@latest <app-name> -- --template react
```
#### Vite & TypeScript
```
$ npm create vite@latest <app-name> -- --template react-ts
```
##### Deploy to a Github pages a React App (Vite)
Install gh-pages
```
$ npm install --save-dev gh-pages
```
Set package.json
```
"homepage": "https://<user>.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d dist"
}
```
Set vite.config.js
```
base: "/<repo>"
```
Run
```
$ npm run predeploy
$ npm run deploy
```
#### CRA
```
$ npx create-react-app <name>
$ cd <name>
$ npm start
```
#### CRA & TypeScript
```
$ npx create-react-app my-app --template typescript
$ npm install --save @types/react
```
##### Deploy to a Github pages a React App (CRA)
Install gh-pages
```
$ npm install --save-dev gh-pages
```
Set package.json
```
"homepage": "https://<user>.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d build"
}
```
Run
```
$ npm run predeploy
$ npm run deploy
```
### Terms and concepts
* React
  - JavaScript library
  - based on components
  - UI
  - client side
  - declarative
  - reactive
  - virtual DOM
  * Unidirectional flow
    - parent to child
  * events
    - nativeEvent
    - SyntheticEvents
  * JSX
    - JSX is a syntax extension (sugar sintactic)
  * UI
    - tree model

* Project structure
  - Structure by default
* Code structure
  - By Feature
  - By Layer
  - MVC

* Components
  * Are regular JavaScript function, but
    - their names always begin with a capital letter
    - they returns JSX markup
  - Never define a component inside another component
  - Always, import or define every component at the top level
  - Every piece of UI is a component
  * Parts
    - Content (html)
    - Presentation (css)
    - Interactivity (js)
  * Nesting and organizing components
    * Export
      - Named
      - By default
    - Import
  * With state or without state
  * Unidirectional, One-way Data Binding
    - Parent to child flow
  * Allow define as class and as function
    - of class
    - functional
  * Communication between components
    - Parent to child (props)
    - Child to parent (event of the son altering the state of the father)
    - Unrelated components

* Components
  * render
    - props
    - state
    - conditional rendering
    - rendering lists
  - fragment
  - reactivity

- Keeping components pure

* Properties ― props (inmutable), it's a object
  - Default Props
  - Props like attribute
  - Prop Types
  - key
* Props
  - Values
  - Children
  - Functions

* State
  - Inmutable
  - Declarative
  - Reactive
  - Asynchronous
  - A functional component can't have state

* Events
  - Native
  - Synthetics
  - Custom

* State
  - Managing state

* Hooks
  - Rules
  - Built-in
  - Own
  - Third

- Lifecycle

* Forms
  - Controlled input element

* Good practices
  - composition instead of inheritance
  - stateless components
  - pattern: container / content
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
