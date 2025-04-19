# :memo: Notes
## ZDOCS
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
## Style Guide
Always use the same coding conventions for all this project to secure quality, improve code readability and make code maintenance easy.
### Python code writing
- Always write the code in English and use clear syntax as much as possible
- Use descriptive names
- Use comments only when necessary
- Use "snake_case" in files name, variables name, functions name, object attributes name
- Use "UpperCamelCase" in classes name
- Avoid lines longer than 80 characters
- Use 4 spaces for indentation
- Put spaces around operators
### JavaScript code writing
- Always write the code in English and use clear syntax as much as possible
- Use descriptive names
- Use comments only when necessary
- Use "lowerCamelCase" in files name, variables name, functions name, object attributes name
- Use "UpperCamelCase" in classes name
- Avoid lines longer than 80 characters
- Use 2 spaces for indentation
- Put spaces around operators
### Python files
Code ordering

1. Imports from core python
2. Imports from core django
3. Imports from core django rest framework
4. Imports from external source
5. Imports from internal source
6. Variables
7. Functions
8. Code execution
### JavaScript files
Code ordering

1. Imports from external source
2. Imports from internal source
3. Variables (only use "let" and "const" keywords, prefer "const" as much as possible)
4. Functions
5. Code execution
### Svelte files
#### Sections
Code ordering

1. Script
2. HTML
3. Style
#### Script section
Code ordering

1. Imports from core svelte
2. Imports from external source
3. Imports from internal source
4. Props
5. Variables (only use "let" and "const" keywords, prefer "const" as much as possible)
6. Reactive variables
7. Lifecycle methods
8. Functions
9. Code execution
### API Responses
Always respond with JSON, keep single structure:

1. result: "successful" or "error", just one of these two strings
2. message: A string according to the case, never an empty string
3. data: According to the case or null, only one of these two options

Sample of a successful case:
```
    {"result": "successful", "message": "Done", "data": null}
```

Sample of an error case:
```
    {"result": "error", "message": "Underdone", "data": null}
```
# Technical documentation
## Getting Started
## Stack
## Understanding environments
## Understanding branches
### Use of branches
## Relationship environments branches
## Deploy
## Running locally
### Requirements
### Optional
### Steps
### Use
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2023  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
