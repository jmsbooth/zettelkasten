# Core Concepts of JavaScript

JavaScript is a powerful programming language that is widely used for web development. Here are some core concepts of JavaScript that you should understand in order to become proficient in this language:

## Variables

Variables are used to store data in JavaScript. You can create a variable using the `var`, `let`, or `const` keyword, followed by the variable name and an optional initial value. **`let` is the most common and recommended way to set variables.**

javascriptCopy code

`var x = 10; let y = "hello"; const z = true;`

You can update the value of a variable using the assignment operator `=`.

javascriptCopy code

`x = 20; y = "goodbye";`

### Variable Scopes

Variables in JavaScript can have two types of scope: global and local. A global variable is accessible from any part of your code, while a local variable is only accessible within the block of code in which it is defined.

javascriptCopy code

`// Global variable var globalVar = "I am global!";  function myFunction() {   // Local variable   var localVar = "I am local!"; }`

## Data Types

JavaScript has several data types, including strings, numbers, booleans, objects, and arrays.

### Strings

Strings are used to represent text in JavaScript, and are enclosed in either single or double quotes.

javascriptCopy code

`var message = "Hello, world!";`

### Numbers

Numbers in JavaScript can be integers or decimals.

javascriptCopy code

`var age = 30; var price = 19.99;`

### Booleans

Booleans in JavaScript represent true or false values.

javascriptCopy code

`var isStudent = true; var isTeacher = false;`

### Objects

Objects in JavaScript are used to store collections of data. They consist of key-value pairs, where the key is a string and the value can be any data type.

javascriptCopy code

`var person = {   name: "John",   age: 30,   isStudent: true };`

### Arrays

Arrays in JavaScript are used to store collections of data, and can contain any data type.

javascriptCopy code

`var numbers = [1, 2, 3, 4, 5]; var colors = ["red", "green", "blue"];`

## Functions

Functions are blocks of code that can be called to perform a specific task. You can create a function using the `function` keyword, followed by the function name, parameters, and the function body.

javascriptCopy code

`function addNumbers(num1, num2) {   return num1 + num2; }`

You can call a function by using its name, followed by parentheses and any necessary arguments.

javascriptCopy code

`var sum = addNumbers(5, 10);`

## Control Structures

Control structures are used to control the flow of code in JavaScript. The most common control structures are `if` statements and loops.

### If Statements

If statements are used to perform different actions depending on a specific condition.

javascriptCopy code

`if (age < 18) {   console.log("Sorry, you're not old enough to vote."); } else {   console.log("You're old enough to vote!"); }`

### Loops

Loops are used to repeat code a specific number of times.

#### For Loops

For loops are used to repeat code a specific number of times.

javascriptCopy code

`for (var i = 0; i < 10; i++) {   console.log(i); }`

#### While Loops

While loops are used to repeat code while a specific condition is true.

javascriptCopy code

`var i = 0;  while (i < 10) {   console.log(i);   i++; }`

## Non-block event looping


## Document Object Model (DOM)
