# Programming and Tech Terminology

This document serves as a comprehensive glossary of essential programming and technology terms. It aims to enhance understanding of key concepts, improve coding skills, and provide clear definitions and examples for common vocabulary used in programming languages, development tools, and web technologies.

---

## Key Elements:
- Use `-` for bullet points to create a list for the definition.
- Use `###` for headings to organize examples.
- Wrap HTML code blocks in triple backticks (```) followed by `html` to indicate the language.
- Inline comments in HTML will still appear in the code block but will be ignored when rendered in a browser.

This format makes it clear and organized, allowing readers to understand the definitions and examples easily.

## Vocabulary Terms

### General Programming Concepts
- **Server**: A computer or system that provides resources, data, services, or programs to other computers, known as clients, over a network. Servers often have a 24/7 listening component, meaning they are continuously available to respond to requests and provide storage or services without interruption.

- **Application**: A software program designed to perform specific tasks or functions for the user.

### Programming Languages & Code Structure

- **Scope**: The context in which variables are defined and accessed in a programming language. It determines the visibility of variables and functions in different parts of the code. 

  ```javascript
  function myFunction() {
    let localVariable = "I'm local"; // Local scope
    console.log(localVariable); // Accessible here
  }
  myFunction();
  // console.log(localVariable); // Error: localVariable is not defined

- **Scope Chain**: The hierarchy of scopes in which a variable can be accessed. When a variable is referenced, JavaScript looks for it in the current scope, and if not found, it checks the outer scopes until it reaches the global scope.

  ```javascript
  let globalVariable = "I'm global"; // Global scope

  function outerFunction() {
      let outerVariable = "I'm from outer function"; // Outer scope

      function innerFunction() {
          let innerVariable = "I'm from inner function"; // Inner scope
          console.log(innerVariable); // Output: I'm from inner function
          console.log(outerVariable); // Output: I'm from outer function
          console.log(globalVariable); // Output: I'm global
      }
      innerFunction();
  }

  outerFunction();
  console.log(globalVariable); // Output: I'm global

- **Block Scope**: A type of scope in programming languages that restricts the visibility of variables to the block in which they are defined, typically enclosed by curly braces `{}`. Variables are created within specific code blocks, such as `if`, `for`, or `while` statements. This scope is limited to the specific block where the variable is declared.

  ```javascript
  //Example: Function Scope
  function exampleBlockScope() {
      let blockVariable; // Declare the variable in function scope
      const constantBlockVar = "I'm block-scoped with 'const'"; // Constant can be declared here if needed

      if (true) {
          blockVariable = "I'm block-scoped with 'let'"; // Assign a value within the block
      }
      
      console.log(blockVariable); // Output: I'm block-scoped with 'let'
      console.log(constantBlockVar); // Output: I'm block-scoped with 'const'
  }

  exampleBlockScope();

  //Example: Block Scope in Conditional Statements and Loops
  function checkCondition() {
    let result = "Before condition";
    if (true) {
        let result = "Inside condition"; // Block-scoped variable
        console.log(result); // Output: "Inside condition" from the inner scope
    }
    console.log(result); // Output: "Before condition" from the outer scope
  }

  checkCondition();

- **Local Scope**: The visibility of variables declared within a function. These variables are only accessible inside that function.
  ```javascript
  function myFunction() {
    let localVariable = "I'm in local scope";
    console.log(localVariable); // Output: I'm in local scope
  }
  myFunction();
  console.log(localVariable); // Error: localVariable is not defined

- **Global Scope**: In JavaScript, **global scope** is the broadest scope available, where variables declared outside any function can be accessed from anywhere in your code, including inside functions and conditional statements. Think of global scope as the "public square" of your program, where everything can be seen and accessed.

  While convenient, using global variables can lead to issues such as naming collisions and unintended modifications, making it important to use them judiciously. Variables declared in global scope have visibility throughout the entire code, allowing them to be accessed from any part of the program.

  1. **Using `let`:**

      ```javascript
      let globalVariable = "I'm in global scope";

      function myFunction() {
          console.log(globalVariable); // Output: I'm in global scope
      }
      myFunction();
      console.log(globalVariable); // Output: I'm in global scope
      ```
  2. **Using `var`:**

      ```javascript
      //Example 1: Access Local Variable
      var globalVariable = "I'm in global scope";

      function myFunction() {
        console.log(globalVariable); // Accessing global variable
      }

      myFunction();
      
      //Example 2: Concept of Variable Shadowing
      var message = "Global message";
      
      function showMessage() {
        var message = "Local message"; // This "shadows" the global variable
        console.log(message); // Accessing the local variable
      }

      showMessage();
      console.log(message); // Accessing the global variable

- **Attribute**: A characteristic or property of an HTML element that provides additional information about that element.

  ```javascript
   <img src="image.jpg" alt="A beautiful image" width="500" height="600"> 

   <a href="https://www.w3schools.com">Visit W3Schools</a>
  ```
   
### Development Tools & Systems

- **Compiler**: A program that translates source code written in a high-level programming language into machine code or bytecode.

- **Assembly Language**: A low-level programming language that uses symbolic code and is closely related to machine code.

### Web & APIs
- **Web Browser**: A software application that enables users to access, retrieve, and view content on the World Wide Web.

- **API (Application Programming Interface)**: A set of rules and protocols for building and interacting with software applications, enabling communication between different systems.

- **DOM (Document Object Model)**: A programming interface for web documents that represents the structure of a document as a tree of objects, allowing programs to manipulate the document's content and structure.

---

## Keyboard Shortcuts

This section lists useful keyboard shortcuts to improve productivity when coding.

### Common Shortcuts (Edit/View Keyboard Shortcut Ctrl+K+S)

- **Alt + Click Multiple Spots**: Enables multi-cursor editing, allowing you to make simultaneous changes in multiple places. *(Ensure it's activated in Visual Studio at Selection > Switch to Alt+Click for Multi Cursor)*

- **F2 + Click**: Renames multiple instances of an identifier simultaneously to streamline refactoring. *(In older Visual Studio versions, use Ctrl + Shift + L)*

- **Shift + Alt + F**: Formats and auto-corrects code in the editor for improved readability and consistency.

---

