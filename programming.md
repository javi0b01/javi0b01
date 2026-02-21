# :memo: Notes
## PROGRAMMING
### Learn
1. What and why
2. What do
3. Why use
4. Getting started
5. Concepts
6. Code samples
7. API documentation
### Resources
- [What is software development?](https://www.ibm.com/topics/software-development)
### Terms and concepts
Index
- [Problem Solving](#problem-solving)
- [Algorithm](#algorithm)
- [Data Types](#data-types)
- [Store Data](#store-data)
- [Operations](#operations)
- [Flow](#flow)
- [Clean Code](#clean-code)
- [Software](#software)
- [Introduction to Programming and Computer Science](#introduction-to-programming-and-computer-science)
- [Programming Logic](#programming-logic)
- [Programming Paradigms](#programming-paradigms)
- [SOLID Principles](#solid-principles)
* [Architecture Patterns](#architecture-patterns)
  - [Project Structure](#project-structure)
- [Design Patterns](#design-patterns)
- [UI Design Methodology](#ui-design-methodology)
- [Cloud](#cloud)

***SDLC*** (Software Development Life Cycle)  
SDLC is the structured process that ensures software is high quality, cost-effective, and delivered on time.  
* SDLC
  - Planning
  - Requirement Analysis
  - Design
  - Implementation (Coding/Development)
  - Testing
  - Deployment
  - Maintenance
* Popular SDLC Models
  - Waterfall → Linear, step-by-step (finish one phase before the next).
  - Agile → Iterative, flexible, with small sprints and continuous feedback.
  - Spiral → Risk-driven, combines prototyping and iterative improvements.
  - V-Model → Focus on testing at each stage.

* SRS (Software Requirements Specification)
  - What the system should do.

* DDS (Design Document Specification) sometimes also called (Detailed Design Specification)
  - How the system will do it (design details)

***CRUX*** (Core Challenge | Critical Problem)  
Crux refers to the core challenge or critical problem  
Identifying the crux helps developers focus on solving the most impactful issues early in the development process.

#### Problem Solving
Problem solving is the core thing software developers do.  The programming 
languages and tools they use are secondary to this fundamental skill.
1. Understand the problem
2. Plan
3. Divide and conquer
* Resources
  - Basic paper and pencil
  - Diagrams
  - Questions
  - Answers
  - Sketch
  - Algorithm
  - Psudocode
#### Algorithm
* Algorithms
  - Independent
  - Definite
  - Precise
  - Finite
  - Input specified
  - Output specified
* Types of algorithms
  - Numeric
  - Not numeric
  - Graphic: Flowchart, Nassi-Schneiderman diagram
  - Not graphic: Pseudocode
* Flowchart
  - Analysis
  * Construction
    - Start, step by step and End
    - ANSI standard
    - Order
    - Symbols
    - Flow lines
  - Desktop test
* Nassi-Schneiderman diagram
  - Analysis
  * Construction
    - Start, step by step and End
    - Order
    - Symbols
    - Flow
  - Desktop test
* Pseudocode
  - Analysis
  * Construction
      - Start, step by step and End
      - Order
      - Line by line
  - Desktop test
#### Data Types
- boolean, int, float, double, char, string
* Only type, not data type
  - Void
* Identifiers
  - Names to store data types
* Units of information
  - Bit, A binary digit, Zero or One
  - Crumb, two bits or quarter byte
  - Nibble, four bits or nybble or half a byte
  - Byte, eight bits or octet
  - Word, set of bytes
  - Kilobyte, 1024 bytes
  - Megabyte, 1024 KB
  - Gigabyte, 1024 MB
  - Terabyte, 1024 GB
  - Petabyte, 1024 TB
  - Exabyte, 1024 PB
  - Zettabyte, 1024 EB
  - Yottabyte, 1024 ZB
  - Memory address
#### Store Data
* Data structures
  * Simple or Primitive
    * Variable
      - type
      - name
      - value or reference
    - Constant
  * Non primitive or Structured
    * Lineal
      - stack, queue, list, array, linked list, hash table
    * Non lineal
      - tree, grafo, dictionary
  - Dynamic
  - Static
  - Initialization
  - Declaration
  - Assignment
  - Scope
  * Efficiency
    - Searching algorithms
    - Sorted
    - Unsorted
    - Worst case scenario O(n), O(log n)
    - Average scenario O(n/2), O(log n)
#### Operations
- Operands
* Operators
  - Arithmetics
  - Assignment
  - Comparison
  - Logical
  - Relational
  - Increment
  - Decrement
  - Grouping
  - Concatenation
  - Identity
  - Membership
  - Bitwise
#### Flow
- Sequential
* Selective
  * Control flow
    - Conditionals
    - Loops
    - Flow handling
* Functions
  - Parameter (variable)
  - Argument (value)
  - Return value
  * Naming a function
    - "show…" usually show something.
    - "get…" return a value.
    - "calc…" calculate something.
    - "create…" create something.
    - "is…" check something and return a boolean.
    - "check…" check something and return a boolean.
    - "verb…" make something, etc.
  - Scope
  * Recursion
    - Base case
    - Recursive case
* Errors
  * Understanding errors
    - Syntax error
    - Runtime error
    - Logic error
  - Resolving errors
* Resolving errors
  - Read the error carefully
  * Debugger
    - Version manager
    - Run program frequently
    - Breakpoint debugging
    - Commenting
  - External resources (Search, forum, etc)
#### Clean Code
- Logic before coding
- Writing clean code
- Consistency
- Indentation
- Line length
* Naming things
  - Variables with a noun or adjetive
  - Functions with a verb
* Comments
  - Explanatory
  - Avoid abusing
- Short functions
- Respecting standards in use
- Avoid indiscriminate mixing of coding languages
- Caution with imports
- DRY (Don't Repeat Yourself)
- Self-explanatory program code, if it is not possible then attach comments.
* Pure function
  - It minds its own business. It does not change any objects or variables that existed before it was called.
  - Same inputs, same output. Given the same inputs, a pure function should always return the same result.
#### Software
- Operating systems
- Applications
- Programs
* Program
  - Programming
    - Modular programming
    - Structured programming
  - Programmer
  - Programming languages
* Programming languages
  - Codification
  - Source code
  - Machine language
  - Low level
  - High level
  - Program structure
  - Syntax
  - Keywords
  - Translators
  - Instructions
* Translator
  - Compiler
  - Interpeter
* Instructions
  - Input
  - Output
  - Calculation
  - Of control
* Statements
  - Values, Operators, Expressions, Keywords, Comments.
* Expressions
  - Values, variables, and operators, which computes to a value.
* Architecture
  - Monolithic
  - Microservices
  - Single Source Of Truth

* Web Site
  - Landing Page, Web Page, Web Site
  - SEO
  - Públic
  - Fast
  - Static
* Web Application
  - Private
  - Logic / Functionality
  - Dynamic
- Leads
- Crawlers
#### Software Engineering
* Software Life Cicle
  * Analysis
    Requirements Specification
  * Design
    - Set of classes (OOP)
  * Coding
    - Implement design
  * Testing
    - Run program
    - Unit testing (OOP)
    - Integration testing (OOP)
    * Debugging
      - Eliminate programming error
  * Operation
    - Use
    - Software maintenance
- Well-designed and -constructed software is easy to maintain.
- It is important to follow the standard naming convention and best practices.
- Software maintenance is easier with easy-to-understand programs.
* SDLC (Software Development Life Cycle)
  1. Planning ...What do we want to build and why?
  2. Requirement Analysis ...What should the software do? SRS (Software Requirements Specification)
  3. Design ...How will the system look and work internally? DDS (Design/Detail Document Specification)
  4. Implementation (Coding/Development) ...Let's build it!
  5. Testing ...Does it work as expected?
  6. Deployment ...Now the users can use it.
  7. Maintenance ...Keep it running and improving.
* SDLC Models
  - Waterfall
  - Agile
  - Spiral
  - V-Model

SDLC is the structured process that ensures software is **high quality, cost-effective, and delivered on time**.

---
#### Introduction to Programming and Computer Science
- Introduction
- What is programming?
- How do we write code?
- How do we get information from computers?
- What can Computer's do?
- What are variables?
- How do we manipulate variables?
- What are conditional statements?
- What are arrays?
- What are loops?
- What are errors?
- How do we debug code?
- What are functions?
- How can we import functions?
- How do we make our own functions?
- What are array lists and dictionaries?
- How can we use data structures?
- What is recursion?
- What is pseudocode?
- Choosing the right language?
- Applications of programming
---
#### Programming Logic
* Programming
  - What
  - Why
  - How
- Human language
  - Idioms
  - Pseudocode
  - Diagrams
  - Desktop testing
- Machine language
* Programming language
  - High level
  - Low level
* Algorithm
  - Start
  - Input
  * Steps
    * Process
      - Operations
      - Conditions
      - Loops
  - Output
  - End
* Data or Information
  - Datum
* Data types
  * Generics
    - Integer
    - Float or Real
    - Logic or Boolean
    - Character / Characters
* Variables
  - Naming
  - Declaration
  - Initialization
  - Assignment
  - Read
  - Write
  - Read and Write
  - Constants
- Input
- Output
- Process
* Operations
* Operators
  - Assignment
  - Arithmetic
  - Relational
  - Logics
* Conditional
  - if
  - if...else
  - Nesting or Multiple
* Loop or Bucle or Cicle or Repetition
  - for
  - while
  * Base condition or Control or exit condition
    - Count
    - Guard
  - Infinite
  - At least once
* Arrays
  - Unidimensional or Vector
  - Multi-Dimensional or Matriz
  - Index
  - Element
  - Length
  - Access the elements
  - Iterate or Go through
* Subprograms
  - Procedural
  - Functions
#### Programming Paradigms
- Paradigm
* Imperative programming paradigm
  - Procedural programming
  * Structured programming
    - Sequential
    - Conditional
    - Repetition
  * Object-oriented programming | [OOP](oop.md)
    - Encapsulation
    - Inheritance
    - Polymorphism
    - Abstraction
    * Classes
      - Instances
    * Objects
      * Attributes
        - Properties or characteristics
        - Methods or actions or behaviours
* Declarative programming paradigm
  - Logic programming paradigms
  - Functional programming paradigms
  - Database/Data driven programming approach
#### Design Principles
* SOLID Principles (Object-Oriented Design Principles)
  * Single Responsibility Principle
    - One task, only one responsibility.
  * Open/Close Principle
    - Open for extensión, close for modification.
  * Liskov Substitution Principle
    - Every subclass or derived class should be substitutable for their base or parent class.
  * Interface Segregation Principle
    - Only require what is used.
  * Dependency Inversion Principle
    - Entities must depend on abstractions, not on concretions.
- DRY (Don't Repeat Yourself)
- Encapsulation
- Composition Over Inheritance
- LoD (Law Of Demeter)
- KISS (Keep It Simple, Stupid)
- YAGNI (You Aren't Gonna Need It)
- SoC (Separation of Concerns)
- Favor Composition Over Inheritance
- CQRS (Command Query Responsibility Segregation)
- TDA (Tell, Don't Ask)
- Don't Call Us, We'll Call You (Inversion of Control)
- Simplicity (Simple vs Easy)

* Benefits
  * Code
    - clean
    - easy to understand
    - flexible
    - adaptable
    - reusable
  - fewer bugs
#### Architecture Patterns
- Monolith
- Microservices
- Microfrontends
- Client-Server
- Model-View-Controller
- Layered
##### Project Structure
###### Backend
- By Feature
- By Layer

MVC
* src
  - models
  - views
  - controllers

MVC by modules
* src
  * xModule
    - models
    - views
    - controllers

By Hexagonal Architecture / Layer
* src
  * domain
    - models
    - services
  * infrastructure
    - components
    - http
    - repositories
  - application

By Packages / Flux
* src
  * packages
    * xPackage
      * src
        - store
        - components
        - actions
        - mutators
  * shared
    * xPackage
      * src
        - store
        - components
        - actions
        - mutators
###### Frontend
Basic
* src
  - css
  - data
  - fonts
  - img
  - js

By Type File
* src
  - components
  - directives
  - hooks
  - pages
  - pipes
  - services

* public
  - register
  - login
* private
  - dashboard
  - profile

By UI
* src
  * render (UI)
    - layout
    - pages
    - sections
    - components
    - UI (shared)
  * logic (no UI)
    - services
    - helpers
    - utils

By Feature
* src
  * features
    * xFeature
      - components
      - directives
      - hooks
      - pages
      - pipes
      - services
  * shared
    - components
    - directives
    - hooks
    - pages
    - pipes
    - services

By Clean Architecture
* src
  - adapters (reusable)
  - assets
  - components (reusable)
  - contexts
  - hooks (reusable)
  - interceptors (reusable)
  - models (reusable)
  * pages
    * xPage
      - adapters (unique)
      - components (unique)
      - contexts
      - hooks (unique)
      - interceptors (unique)
      - models (unique)
      - services (unique)
      - styledComponents (unique)
  - redux
  - services (reusable)
  - styledComponents (reusable)
  - utilities

By Routes
* src
  * pages
    - xRoute
  * core (no UI)
    - guards
    - interceptors
    - models
    - services
  * shared (UI)
    - components
    - directives
    - hooks
    - pages
    - pipes
    - services

By Atomic Design
* src
  * features
    * xFeature
      - atom
      - molecule
      - organism
  * shared
    * components
      - atom
      - molecule
      - organism
    - hooks
#### Design Patterns
- Singleton
- Factory
- Observer
#### UI Design Methodology
* Atomic Design System
  * Atom
    * Subatomic elements
      - Fonts
      - Typography
      - Colors
      - Shadows
      - Animations
  * Molecule
    - Atoms
  * Organism
    - Atoms
    - Molecules
  * Template
    - Atoms
    - Molecules
    - Organisms
  * Page
    - Atoms
    - Molecules
    - Organisms
    - Templates
  * Website
    - Atoms
    - Molecules
    - Organisms
    - Templates
    - Pages
- Design Thinking
- Agile UX
- Lean UX
- Material Design

* Debugging
  - Use a debugger
  - Use git bisect
  - Ask a rubber duck
  - Check logs
  - Systemativally fix the bugs
  - Reproduce the failure to ensure the bug is fixed

* Testing
  - given
  - when
  - then
  - Pruebas unitarias
  - Pruebas funcionales
  - Pruebas end to end
  - Análisis de código estático
  - Jest, Jasmine, Cypress, Selenium
  - pruebas automatizadas
  - JUnit, Mockito y herramientas de pruebas de integración como TestContainers
### Cloud
* Location
  - On-Premise
  - Cloud Computing
  - Hybrid
  - Intercloud Exchange
- IaaS (Infrastructure as a Service)
- PaaS (Platform as a Service)
- SaaS (Software as a Service)
- Cloud Providers
* AWS (Amazon Web Services)
  - EC2 (Elastic Cloud Computing)
  - S3
  - VPC (Virtual Private Cloud)
  - Lambda
  - CloudFront
  - Server
  - Instance
  - VM (Virtual Machine)
  - Amazon Machine Image (AMI)
  - Auto Scaling
  - Load Balancing
  - DoS (denial-of-service)
  - Route 53
  * IP's
    - Private
    - Public
  - Serverless
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
