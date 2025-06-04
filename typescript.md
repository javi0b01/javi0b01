# :memo: Notes
## TYPESCRIPT
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [TypeScript](https://www.typescriptlang.org/)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [TypeScript Cheat Sheets](https://www.typescriptlang.org/cheatsheets)
- [DOM Manipulation](https://www.typescriptlang.org/docs/handbook/dom-manipulation.html)
- [DOM type definitions](https://github.com/microsoft/TypeScript/blob/main/src/lib/dom.generated.d.ts)
- [Node TypeScript Cheatsheets](https://github.com/typescript-cheatsheets/node)
- [React TypeScript Cheatsheets](https://react-typescript-cheatsheet.netlify.app/)
- [Vue TypeScript Cheatsheets](https://github.com/typescript-cheatsheets/vue)
### Requirements
- Nodejs
#### Install
Global
```
$ npm install -g typescript
$ tsc -v
```
##### Setup within a new npm project
Create a new npm project
```
$ npm init -y
```
Installing the Compiler
```
$ npm install typescript --save-dev
```
Configuring the compiler
```
$ npx tsc --init
```
tsconfig.json file
```
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "./",
    "outDir": "./",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  },
  "include": [
    "index.ts"
  ],
  "exclude": [
    "node_modules"
  ]
}
```
index.ts file
```
console.log("Works!")
```
Run compiler
```
$ npx tsc
```
##### Setup
Project
```
$ tsc --init
```
tsconfig.json file
```
{
  "compilerOptions": {
    "target": "esnext",
    "experimentalDecorators": true,
    "emitDecoratorMetadata", false,
    "useDefineForClassFields": true,
    "module": "commonjs",
    "noImplicitAny": true,
    "removeComments": true,
    "preserveConstEnums": true,
    "sourceMap": true,
    "outFile": "../../built/local/tsc.js",
    "sourceMap": true
  },
  "include": ["src/**/*"],
  "exclude": ["**/*.spec.ts"]
}
```
###### Basics
```
$ npm install --save-dev typescript
$ node_modules/.bin/tsc --init
$ node --save-dev
```
### Basic Commands
```
$ tsc -v
$ tsc <file name>
$ tsc -w
$ tsc <file name> -w
$ tsc --init
$ tsc *.ts -w
$ tsc --watch
```
### Terms and concepts
- ECMAScript
- JavaScript
- TypeScript
- Transpile
- Compile

* Data Types
  * Primitives
    - boolean
    - number
    - string
  * Special
    - undefined
    - null
    - any
    - unknown
    - never
    - void
  * Complex
    - array
    - tuple
    - object
    - enum
    * Generic
      - utility
      - custom
  * Custom
    - class
    - interface
    - type
  - Inference
  - Alias
  - Literals
  - Union
  - Discriminating Unions
  - Intersection Types
  - Implicit
  - Explicit
  - Casting or overriding
  - Enums

- Shape

* Functions
  - Optional parameter
  - Default argument
  - Return type
  - Signature
  * Param and return
    - Types
    - Type Inference

* Classes
  - Properties
  * Methods
    - constructor
  * Modifier
    - protect
    - readonly
    - abstract
  * Instance
    - this
  * Visibility
    - public (default)
    - private
    - protected
  * Virtual attributes
    - setter
    - getter
    - accessor

* Interfaces
  - Contract | Agreement
  - Attributes
  - Functions
  - Modifiers
  - Inheritance

- Inheritance

* Hierarchi
  - super
  - overwrite

- Encapsulation

* OOP
  - Hierarchi
  - Encapsulation
  - Polymorphism
  - Abstraction

* Decorator
  - Class
  - Method
  - Property
  - Parameter

* Utility types or helpers
  - Partial
  - Required

- Custom Type

* Generic Type
  - Data type
  - Function
  - Class
  - Interface

- Union types

* Modularity
  - Settings
  - Export
  - Import

* Projects
  - tsconfig

* DOM Manipulation
  * HTMLElement
    - HTMLParagraphElement
  * Methods
    * children
      - HTMLCollection
    * childNodes
      - NodeList
  - The ! non-null assertion operator
  - Type casting
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
