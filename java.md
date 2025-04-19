# :memo: Notes
## JAVA
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Java SE & JDK Version 22 API Specification](https://docs.oracle.com/en/java/javase/22/docs/api/index.html)
- [Java](https://www.java.com/)
- [Java SE API v7](https://docs.oracle.com/javase/7/docs/api/)
- [Code Conventions](https://www.oracle.com/java/technologies/javase/codeconventions-contents.html)
- [Java SE JDK v11 API](https://docs.oracle.com/en/java/javase/11/docs/api/index.html)
- [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html#s7.1-javadoc-formatting)
- [The Java Tutorials](https://docs.oracle.com/javase/tutorial/index.html)
- [OpenJDK](https://openjdk.org/)
- [IntelliJ](https://www.jetbrains.com/idea/)
- [NetBeans](https://netbeans.org/kb/)
- Java Doc
### Requirements
#### Java Installation on Ubuntu system
Default
```
$ sudo apt update
$ java -version
$ apt install default-jre
$ javac -version
$ sudo apt install default-jdk
```
OpenJDK
```
$ sudo apt-get install openjdk-21-jdk
$ sudo update-alternatives --config java
$ javac -version
$ java -version
```
### Terms and concepts
- J2SE (Java2 Standard Edition)
- J2EE (Java2 Enterprise Edition)
- IDE (Integrated Development Environment)
- JVM (Java Virtual Machine)
- JRE (Java Runtime Environment)
- JDK (Java Development Kit)
- OOP (Object-oriented programming)
- Garbage Collector | Deal-locate unused space
* Classes
  - Java System | Java Core
  - Programmer-defined | Standard | System
* Source file (.java)
  * Code Comments
    - Single-line, Multi-line, Java Doc
    - Comment markers
  - The main Class
  - The main Method
  * Interaction
    * Standard input (System.in)
      - Scanner
    * Standard output (System.out)
      - print, println
- Compile the source file (javac)
- Bytecode (.class)
- JIT (Just In Time compiler)
- WORA (Write Once, Run Everywhere)
- Run the program (java)
* Errors
  - Syntax
  - Compilation
  - Execution
* Main features
  - Distribuited
  - Interpreted
  - Multi-threaded
  - Object oriented
  - Platform independent
  - Strongly typed
  - Case sensitive
  * Uses
    - Console application
    - General purpose
    - Applets
* Syntax
  - Keywords
  - Code conventions
  - File names
  - Class names
  - Classes
  - Sentence
  * Access modifiers
    - Default (Package), Private, Protected, Public
  * Scope
    - Package, Class, Subclass, All
* Variables
  - Identifiers
  - Final Variables
  - Scope
  - Type Inference
* Data types
  * Primitive
    - byte
    - short
    - int
    - long
    - float
    - double
    - boolean
    - char
  * Non-primitive or reference types
    - String
    * Array
      - Vector
      - Matriz
      - array vs ArrayList
    - Class
    - Interface
    * (import package)
  * Special
    - Type ```enum```
  * Casting
    * Type Casting
      - Widening Casting (automatically) smaller to larger
      - Narrowing Casting (manually) larger to smaller
    * Ways
      - Automatically
      - Manually
* Data structures
  - Variable
  - Constant
- Boolean expressions
* Operators
  - Assignment
  - Arithmetic
  - Comparison
  - Logical
  - Bitwise
  - Increment and decrement (pre and post)
  - Concatenation
* Control structures
  - Sequential
  * Conditional
    - if
    - if...else (too short hand or Ternary Operator)
    - if...else if...else
    - switch
  * Loop
    - for
    - for-Each
    - while
    - do/while
    - Nested loops
    * Control
      - Counter
      - Guard
  * Flow handling
    - Break
    - Continue
* Some Built-in classes
  * The class Object is super class in Java
    - All classes in Java by default "extend" the Object class
  * String
    - Concatenation
    * Special characters
      * Escape character
        - Escape sequences
    - Methods
    - Access the characters of a String
    - Format
    - Text block
  * Array
    - Access the elements of an Array
    - Methods
    - Property
    - Multi-Dimensional Arrays
    - Iterate
  * Math
    - Methods
  - Thread
  * ... Java API
    * Package
      - Default (java.lang), ...more packages(import)
      - Classes
* Methods or Functions
  - Pre-Defined methods
  - Own or Custom methods
  - Call operator
  - Parameters
  - Arguments
  - Return
  - Overloading
  - Scope
  * Recursion
    - Halting condition
- OOP (Object-oriented programming)
* Model class (structure, template)
  - Instance (object)
* Classes
  - Class Definition
  * Access modifier or Visibility modifier
    - default or package-private
    - public
    - private
    - protected
  * Constructor method
    - Default constructor method
    - Define constructor method
  - this
  - Setter method
  - Getter method
  - Instances
  - Objects
  - Type Inference
  * Methods
    * Parts of a method
      - Range modifier
      - Usage modifier
      - Return type
      - Method name
      - Method body
      - Parameters
    - Operator this
  - Generic class
  - Inner class
  - Local inner class
* Object
  * Attributes
    - Propierties/Characteristics
    - Methods/Actions/Behaviours
  - State
- Modularity
- Encapsulation
* Inheritance
  - Superclass
  - Subclass
  - Only one inheritance, not multiply
  * Annotations
    - @Override
  * Design inheritance
    - Rule "It is a/an..."
  - Polymorphism
  - Casting objects
  * Stop inheritance with ```final```
    - Class
    - Method
  * Abstract
    - Class
    - Method
* Interfaces
  - Abstract methods
  - Constants
- Package
* ArrayList
  - array vs ArrayList
  - Methods
  - Loop through an ArrayList
* Constructors
  - Default
  - Custom
  - Parameters
* Build automation tools
  - Maven
  - Gradle
  - Ant
- JAR (Java Archive)
* Collections
  * Interfaces
    - List
    - Set
    - Queue
    - Map
  - Abstrac class
  * Concret class
    - ArrayList
    - LinkedList
    - HashSet,
    - TreeSet
    - HashMap
    - TreeMap
  - Nested
  * streams
    - Intermediate operations
    - final operations
* Container Object
  - Opctional
* Functions
  - Lambda or anonymous
* Constructors
  - Custom constructor
- Dates

* FIFO / First In, First Out
  - Queue
  - ArrayList
  - LinkedList
* LIFO / Last In, First Out
  - Stack

Map
HashMap
Generics

- JDBC or Java Database Connectivity
- DAO or Data Access Object

* Maven
  - pom or Project Object Model file

- Spring
- Hibernate
- ORM or Object-Relational Mapping
- HQL or Hibernate Query Language
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
