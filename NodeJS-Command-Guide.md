# Node.js Command Guide

This document provides essential commands for working with Node.js projects.

## Checking Installation

Before you start, ensure that Node.js and npm are installed on your system by running the following commands in your terminal:

```bash
node -v  # Check the installed version of Node.js
npm -v   # Check the installed version of npm
#If error, download Node at https://nodejs.org/en, then test in terminal if Node works.
```

## Basic Commands

- **`node index.js`**: Run a JavaScript file with Node.js.
  
**Steps Example:**

1.**Test Run JavaScript by Node**
  ```bash
  npm install       # Install all necessary dependencies defined in 'package.json'
  npm start         # Run the startup script defined in 'package.json'
  node index.js       # Run the 'app.js' file with Node.js
  npm test          # Run the test script, often used to execute test cases
  node fileName.js  # Run another JavaScript file with Node.js
  ```
## Example `index.js` Code

Here are three examples of `index.js` code snippets to demonstrate basic functionality:

### 1. Function to Print "Hello, World!"

This example demonstrates a simple function that prints "Hello, World!" to the console.

```javascript
function greet() {
    console.log("Hello, World!");  // Print 'Hello, World!' to the console
}

greet();  // Call the function to execute
```
```outcome
kimag@KimsDesktop MINGW64 ~/desktop/Test (master)
$ node index.js
Hello, World!
```
###  2. Arrow Function to Print a Message

In this example, we use an arrow function to print a message passed as an argument.

```javascript
var hello = (msg) => {
    console.log(msg);  // Print the message passed to the function
};

hello("Hello Node with Arrow Function");  // Call the arrow function with a message
```
```outcome
kimag@KimsDesktop MINGW64 ~/desktop/Test (master)
$ node index.js
Hello Node with Arrow Function
```
### 3. Demonstrating setTimeout with this in JavaScript

In this example, we will explore how this behaves differently in regular functions versus arrow functions when used within a setTimeout.

```javascript
var person = {
    name: "will",
    saySomething: function() {
        console.log("inside the function -->", this.name);
        
        setTimeout(() => {
            console.log("inside the timeout -->", this.name);
        }, 100);
    }
};

person.saySomething();
```
```outcome
kimag@KimsDesktop MINGW64 ~/desktop/Test (master)
$ node index.js
inside the function --> will
inside the timeout --> undefined
```
## Exiting Node.js or Server Processes

- **`Ctrl + C (twice)`**: Forcefully exit a running Node.js process or server.

  - Pressing `Ctrl + C` once will attempt to gracefully stop the process.
  - Pressing `Ctrl + C` twice will immediately terminate the process.
  
  Example:
  ```bash
  # To stop a running Node.js server
  Ctrl + C (once) # Graceful stop
  Ctrl + C (twice) # Forceful exit
