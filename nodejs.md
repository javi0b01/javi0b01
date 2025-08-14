# :memo: Notes
## NODEJS
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Node.js](https://nodejs.org)
* Node Version Manager
  - [nvm](https://github.com/nvm-sh/nvm)
  - [NVM for Windows](https://github.com/coreybutler/nvm-windows)
  - [n](https://github.com/tj/n)
  - [fnm](https://github.com/Schniz/fnm)
* Node Package Manager
  - [npm](https://www.npmjs.com/)
  - [pnpm](https://pnpm.io/)
### Node
Verify
```
$ node -v
$ npm -v
$ node <file>
$ node --watch <file>
```
Install package
```
$ npm install <name>
$ npm install express --save
$ npm install <name> --save-prod / -P
$ npm install <name> --save-dev / -D
$ npm install <name> --global / -g
```
Uninstall package
```
$ npm uninstall -g <name>
$ npm uninstall <name>
```
Clear chache
```
$ npm cache verify
$ npm cache clean --force
```
### NVM
Install
```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
$ nvm -v
$ nvm install --lts
$ nvm ls
$ nvm ls-remote
$ nvm install vA.B.C
$ nvm use vA.B.C
```
### pnpm
Install
```
$ npm install -g pnpm
```
Verify
```
$ pnpm -v
```
### Terms and concepts
* Node.js
  * Fork
    - io.js
  * JavaScript runtime environment
    - Based on JS language
    - Built on Google's V8 engine for Backend
    - Interpeter
    - Based around events
    - Multiplatform
    - Asynchronous
    - I/O model
    - Asynchronous non blocking model
  * Asynchronous non blocking model
    - Synchronous, parallelism, simultaneous
    - Asynchronous, concurrence, alternate
    - Blocking
    - Non-blocking
    - Reactor design pattern
  * Single thread
    - Based on callbacks
    - Event loop

* REPL

* Good practices
  * Order
    - Libraries, Modules
    - Constants
    - Objects, Variables
    - Functions
    - Events
    - Executions
    - Mode strict
  * Prefer
    - lowerCamelCase
    - Single quotes

* Modules
  * Types
    - Core modules
    - Local modules
    - Third-party modules

* Core modules or Built-in modules
  - Stability level
  * Some modules of the core
    - Globals
    - Process
    - OS
    - File System
    * Events
      - Action into app
      - Define
      - Emit
      - Listen
      * EventEmitter
        - Emitters
      - Event Handler or Event Listener
    * HTTP
      * Model: client-server
      * HTTP protocol
      * Port
      * Request
        - Methods HTTP or Verbs HTTP
      * Response
        - Status codes HTTP
      - CRUD (Create, Read, Update, Delete)
    - URL
    - Routing
    - Buffer
    - Stream
    - Util
    - Timers
    - Path
    - Query String
    - Sniffer
    * Forms
      - GET
      - POST
    - Debugger
    - readLine
    - assert
    - v8

* Third-party modules

* NPM (Node Package Manager)
  - Package
  - Module
  - Dependency
  * Types packages
    - Globals
  * Installing packages
    - Unique: ```npm install <package_name>``` (not recommended)
    - Global: ```npm install <package_name> -g```
    - Project dependency: ```npm install <package_name> --save``` (package.json)
    - Development dependency: ```npm install <package_name> --save-dev``` (package.json)
  * Uninstalling packages
  * package.json
    - ```npm init``` (for a new project)
    - ```npm install``` (for an existing project)
  * package-lock.json
    - autogenerate when package.json or tree node_modules is modify
    - hold record of all dependencies
    - describe the tree generate for next installations
    - contain details

* Promises
  - pending
  - resolve
  - reject
  - then
  - catch
  - chaining promises
  - async
  - await

* Callback function

* Method chaining

* Inheritance

* Classes
  - class
  - constructor
  - extends
  - static
  - getter
  - setter
  - private field
  - public field

* Middlewares
  - Are functions that running after request and running before response.
  - Are functions that have access to the request object (req), the response object (res) and the next() function.
  * Scope
    - Global
    - Local
  * Type
    - Filters
    - Provider

* Some middlewares
  * Built-in
    - static
  * External
    - favicon
    - logger
    - cookie-parser
    - cookie-session
    - body-parser

* Full Stack JavaScript Developer
  - JAM stack (Javascript, APIs, Markup)
  - MERN stack (MongoDB, Express, React, Node)
  - MEAN stack (MongoDB, Express, Angular, Node)
  - MEVN stack (MongoDB, Express, Vue, Node)
  - MESN stack (MongoDB, Express, Svelte, Node)

### Best practices for Node.js + TypeScript projects using ES modules:
1. Use explicit file extensions (.js) in all local imports.
2. Keep environment variable loading (dotenv.config()) at the entry point only.
3. Organize code by feature: e.g., src/routes, src/controllers, src/models, db.
4. Use async/await for database and network operations.
5. Handle errors gracefully (try/catch, error middleware).
6. Validate environment variables and fail fast if missing.
7. Keep configuration (e.g., port, DB URI) in environment variables.
8. Write type-safe code and enable strict mode in TypeScript.
9. Use linter and formatter (ESLint, Prettier) for code quality.
10. Document your API and code (README, comments, JSDoc).
11. Write tests for critical logic (Jest, Mocha, etc.).
12. Use version control (Git) and meaningful commit messages.

## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
