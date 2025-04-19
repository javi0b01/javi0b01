# :memo: Notes
## JAVASCRIPT
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript and HTML DOM Reference](https://www.w3schools.com/jsref/default.asp)
- [JavaScript at Microsoft](https://docs.microsoft.com/en-us/javascript/)
- [The Modern JavaScript Tutorial](https://javascript.info/)
- [JavaScript Tutorial](https://www.javascripttutorial.net/)
- [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)
- [Web technology for developers](https://developer.mozilla.org/en-US/docs/Web)
- [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- [HTMLElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)
### Requirements
- A browser or server environment
### Terms and concepts
* ECMAScript
* JavaScript
* JavaScript uses
  - Web language
  - Interactive
  - Validate
  - Process
  - Front-End
  - Back-End
  - Desktop apps
  - Mobile apps

* script
  * The script tag
    - async
    - defer
  - External file
  - Comments
  - Syntax
  - Reserved Words
  - Keywords
  - Strict mode
  - Sloppy mode
  * The noscript tag

* Debugging
  - ```console```
  - Browser debugging tools
  * Snippets 
    - performance.now
  - debugger

* Statements
  - Values, Operators, Expressions, Keywords, and Comments.

* Expressions
  - values, variables, and operators, which computes to a value.

* Variables
  * Stages
    * Declaration
      - Single
      - Multiple
    - Initializing
    - Modification
  - Hierarchy
  - Scope
  - Hoisting
  - Context
  * Coercion
    - Implicit
    - Explicit
  - Constants

* Data types
  * Primitives:
    * String
      - Used with objects
    - Number
    - Boolean
    - null (Special primitive)
    - undefined
    - Symbol (Descriptions)
    - BigInt
    - NaN - Not a Number
  * Non-primitive or Reference Types:
    - object (for more complex data structures)
    * All types of objects
      - All JavaScript values, except primitives, are objects.
  * Operators
    - typeof
    - instanceof

* Stack & Heap
  * Stack
    - Store value of primitives types
    - Have space limited
    - Store reference to non primitives types (pointer)
  * Heap
    - Store value of non primitives types

* Data structures
  * Arrays
    - Array of objects
    - Matrix, 2D array or more
  * Objects (Special non-data)
    * Propierties
      - Key, Value
      - getter
      - setter
      - prototype
      - call
      - apply
    * Tools
      - freeze
      - seal
  * Sets
    - WeakSets
  * Maps
    - WeakMaps
  * Proxies
    - Handler
  - Functions (non data structure)

* Operators
  - Unary
  - Binary
  - Operand
* Operands
* Operations

* Operators
  * Arithmetic operators
    - PEMDAS (Parentheses, Exponent, Multiplication, Division, Addition, Subtraction)
  - Increment operators
  - Decrement operators
  - Assignment operators
  - Comparison operators
  - Reverse boolean result
  - Logical Operators
  - “Unary +” Operator
  - Bitwise Operators
  - Short circuit operators
  - Spread operator or Rest operator
  - Grouping
  - Concatenation
  - Type coercion
  - Type Operators
  - Constructor

* Control structures
  - Sequential
  * Conditional
    - Boolean logic
    - Comparisons
    - Strict equality check
    * Truthy
      - All values are truthy unless they are defined as falsy.
    * Falsy
      - false, 0, -0, 0n, "", '', ``, null, undefined, NaN and document.all
    * Statements
      - if
      - if ... else
      - if ... else if ... else
      - switch
      - Ternary operator
  * Loops
    - Do While
    - While
    - For
    - For ... in
    - For ... of
    - ForEach
    - map
    - filter
    - "own loop"
    * Iterator object
      - keys
      - values
      - entries
  * Flow handling
      - Break
      - Continue

* Errors
  * Anatomy (is an object)
    * name/type
      - SyntaxError
      * Logic errors
        - ReferenceError
        - TypeError
    * message
      - Describe causing
    - file name
    - row or line
    - column or character
    - stack trace
  * Error handling
    - Try ... Catch ... Finally
    - Throw

* Destructuring
  - Assign by Destructuring
  - Destructuring, Functions, Arrays and Objects

* Objects
  * Basics
    - What are they?
    - Syntax
    - Definition (literals, constructor)
  * Propierties
    - Attributes
    - Methods
  - Dot notation
  - Square bracket notation
  - this keyword (context)
  * Binding
    - Implicit
    - Explicit
    - New
    - Window
  * Object literal (it is the opposite of destructuring)
    - Static and nonreusable
  * Object constructor
    - Dynamic and reusable
  - Static object

* this keyword (context)
  - this context: is a reference according to the context
  - Functions needs access to runtime context.
  - "this" maps to relevant context at runtime
  * What is "this"?
    - In JavaScript, this keyword refers to an object.
    - Which object depends on how this is being invoked (ised or called).
    * The this keyword refers to different objects depending on how it is used:
      * In an object method:
        - In a regular function, this refers to the object.
        - In a arrow function, this refers to the global object.
      - Alone, this refers to the global object.
      - In a function, this refers to the global object.
      - In a function, in strict mode, this is undefined.
      - In an event, this refers to the element that received the event.
      - Methods like "call" "apply" and "bind" can refer this to any object.
  - this is not a variable, it is a keyword.

* About the global object
  - Default to "window" object in browser runtime
  - Default to "global" object in Node.js runtime
  - use "globalThis" keyword to reference the global object consistenly

* Built-in objects
  * Basics
    - The constructor property returns the function that created the JavaScript object prototype.
    - prototype allows you to add new properties and methods to JavaScript objects.
    - prototype is a property available with all JavaScript objects.
  - String
  - Number
  - Boolean
  - Array
  - Object
  - Math
  - Date
  - Set
  - Map
  - Function
  - Promise

* String
  - Single, double and backtick quotes
  - Scaping characters
  - Case sensitive
  - Index
  - Length
  - Properties
  - Methods
  - Concatenating strings

* Number
  - Properties
  - Methods
  - Convert string to number

* Boolean
  * Truthy
    - All values are truthy unless they are defined as falsy.
  * Falsy
    - false, 0, -0, 0n, "", '', ``, null, undefined, NaN and document.all
  - Properties
  - Methods

* Array
  - Element
  - Index
  - Length
  - Populating
  - Properties
  - Methods

* Object
  - Properties
  - Methods

* Math
  * Properties
    - PI
  * Methods
    - round

* Date
  - Properties
  - Methods
  - One central object, contain both Date and time
  - Internally time is stored as number of milliseconds since 1 Jan 1970
  - month counting starts with zero, Sunday = 0
  - 24 hour clock

* Set
  - Properties
  - Methods

* Map
  - Properties
  - Methods

* Promise
  - Properties
  - Methods

* JavaScript Object Notation or JSON
  * Basics
    - What is it?
    - JSON format
    - Serialize Object to JSON (Stringify)
    - Deserialize JSON to Object (Parse)
  - Properties
  - Methods

- Template literals or template strings or literal strings
- Fragments
- Templates and "clone"
- REST parameters (to received)
- Spread operator (to send)

* Functions
  * Basics
    - What are they?
    - Syntax
    - Definition
    - Invocation
    - Naming
    - Parameters
    - Return
  * Function
    * With arguments
      - Parameter list
    * Without arguments
      - No parameter list
  - Implicit return or default return
  * Built-in
    * Interaction methods I/O
      - prompt
      - confirm
      - alert
      - write
      - console
  - Function declaration (search in the same object, in the current object)
  * Function expression
    - Regular function
    - Arrow function (search in the global window)
  - Call function
  - Parameters function
  - Arguments function
  - Parameters by default
  - Anonymous function
  - Self-executing anonymous function
  - IIFE or Immediately Invoked Function Expression
  - Constructor function
  - Generator function (return an iterator)
  - IIFE function (runs as soon as it is defined)
  - Async Await
  - Callbacks
  - Promises
  - First-class function
  - Pure function
  - Methods

* Hoisting
  - hoist variable declaration (not initialization)
  - hoist functions declared
  - Register/Record
  - Execute

* Scope
  - Lexical scoping or static scoping
  - Scope chain
  - Global
  - Function
  - Block
  - Module

* Call Stack
  - LIFO (Last In First Out)
  - Stacktrace
  * Execution contexts
    - Global execution context
    - Function execution context

* Closures
  - retorna una función desde otra función, con acceso al entorno de variables 
  de un ámbito exterior
  - Ex:
```
function IamAclosure() {
  const varLocal = 'xyz'
  return function() {
    return varLocal.toUpperCase()
  }
}

const closure = IamAclosure()
```

* IIFE or Inmediately Invoked Function Expression

* Callback
  - Synchronous
  - Asynchronous

* Prototypes
  * Constructor object or constructor function
    - Dynamic and reusable
  - Object prototype (better with function declaration for the scope)
  - Prototype chain
  - Prototypical inheritance

* Syntactic sugar
  - Prototypes - Classes

* OOP
  * Classes
    - Declaration class
    - Expression class
    - Attributes or Properties
    - Methods
    - Static methods
    - Constructors
    - Inheritance
    - super
    - Scope chain
    - Private attributes or properties
    - Private methods
    - Setters
    - Getters
    - Overwrite methods
    - Polymorphism
  - Maps

* strict mode
  - avoid create global variables accidentally
  - readonly attributes
  - objects not extensibles
  - avoid duplicate parameters
  - octal system, octal literal
  - avoid errors with delete operator
  - 'arguments' and 'eval' are keywords
  - 'with' statement not allowed
  - more keywords
  - free functions

* Prototype
  - Prototypical inheritance

* Regular Expressions

* Modules
  - module
  - nomudule
  - Import
  - Export
  - Export default
  - Alias

* Code ordering
  - Import modules
  - Variables
  - Functions
  - Executables

* Timers
  - TimeOut
  - ClearTimeOut
  - TimeInterval
  - ClearInterval

- Synchronous
- Asynchronous

* Asynchronous
  * Certain operations can take a while
    - File I/O
    - REST calls
    - Database operations
    - Complex computations
  - I/O
  * Single thread
    - One worker process
    - One activity at a time
    - No other tasks can execute
    - User interface or application could appear frozen
  - Multi thread
  - Event loop
  - Stack
  - LIFO
  - Concurrence
  - Parallelism
  - Blocking
  - Non-blocking

* Callbacks
  - Callback hell, cascading becomes an issue

* Promises
  - Pending
  - Fulfilled
  - Rejected
  * Resolve
    - Then
  * Reject
    - Catch
  * Methods
    - all

* Async/Await
  - Make asynchronous code look synchronous
  - Recomended use Try/Catch

* Recursive
* Trampoline (technique)
* Closure

* Iterables & Iterators
  - next
  - done

* Generators
  - yield

* Async functions

* Reactivity
  * State (the data at a specific time)
    * UI based on state
      - change data, then, change content (reder)
  * Component (visual pattern, independent code snippet)
    - reusable
    - unique function
    - independent
    - self-contained

* Window
  - This, Self and Window
  - Global
  * Scope
    - Call
    - Apply
    - Bind

* API (Application Programming Interface)
  * Web APIs
    - Console
    - DOM (Document Object Model)
    - CSSOM (CSS Object Model)
    - BOM (Browser Object Model)
    - Fetch
  - External APIs

* API's Architectures
  - REST (Representational State Transfer)
  - SOAP (Simple Object Access Protocol)

* DOM (Document Object Model)
  - Created by the browser
  * "document" object
    - Properties
    - Methods
  - Allow interacting with the browser

* DOM Nodes
  * Node is an object with properties and methods
    * Properties
      - Like ids, classes, styles, texts, etc
    * Methods
      - For finding/adding/removing/altering or handle on manipulating
  * tree nodes
    - "html" is the root node
  - nodelist
  - array of nodes
  - Elements
  - Traversing
  - Fragments

* DOM Events
  - Allow handle on manipulating the DOM dynamically, or on demand
  - Listeners
  - Remove

* DOM Event flow
  - Propagation
  - Bubble
  - Capture
  - Stop propagation or stop bubbling
  - preventDefault

* DOM Event delegation

* Responsible and Responsive
* User Agent

* CORS (Cross-Origin Resource Sharing)
* HTTP response status codes
* HTTP verbs

* XML
* JSON
* AJAX
  - ActiveXObject
  - XMLHTTPRequest
* Fetch
  - With Async Await
* Axios
  - With Async Await

* SPA (Single Page Application)

* PWA (Progresive Web Application)
  - Fast
  - Instalable
  - Offline support
  * Requeriments
    - Manifest
    - Domain
    - Fetch event listener

* Service Workers
  - Base of the PWA
  - Working offline
  - Not access the DOM
  - Automatly load
  - Work without interferir

* Functional JS
  - Inmutability
  - Separate data functions
  - First-class functions

* Higer order functions
* Pure function
* Closure
* Partials, Currying
* Composition

* Engine
  - Source
  - AST (Abstract Syntax Tree)
  - Bytecode
  - Machinecode

* Event loop
  * Stack FILO
    - push
    - pop
  - Heap
  * Queue FIFO
    - Scheduled tasks (e.g. setTimeout)
    - Microtask queue (e.g. Promises)
    - task queue

* Design Patterns
  * Create code
    - Class Pattern
    - Constructor Pattern
    - Singleton Pattern
    - Factory Pattern
  * Organize code
    - Module Pattern
    - Mixin Pattern
    - Namespace Pattern
    - Mediator Pattern

* Hashing
  - Auth
  - bcrypt

* Tools
  - Babel
  - ESLint
  - Webpack
  - Gulp
  - Style guide (Standard, Google, Airbnb)

* Testing
  - Test Driven Development or TDD
  * Techniques
    - Integration
    - End to End
    - Unit
    - Static
  * Tools
  - Jest
  - Cypress

* Packages are also called dependencies or modules
  - npm or Node Package Manager
  * package.json file
    - Metadata
    - Dependencies and devDependencies
    - Scripts
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
