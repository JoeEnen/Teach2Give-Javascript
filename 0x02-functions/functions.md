# Functions
- is a reusable block of code that performs a specific task. Functions help in writing modular, maintainable, and efficient programs. Instead of repeating the same logic multiple times, we can write a function once and use it whenever needed.
- functions are first-class citizen.
- they can be:
1. Assigned to variables
2. Passed as arguments to other functions
3. Returned from other functions
4. Stored in objects and arrays

## Declaring and Calling Functions
- functions are defined using the function keywords, followed by a name and parentheses (). The function body contains the code that will execute when the function is called.
eg. 
function printHello() {
    console.log("Hello, world");
}

*Calling the function*
printHello();

## Parameters vs arguments
- parameters are variables defined in a function’s parentheses. They act as a placeholder for incoming values. An argument is the actual value passed when calling the function.
eg. 
function greet(name) { *"name" is a parameter*
    console.log(`Hello ${name}`);
}

greet("Joe"); // *Joe is an argument*
- *Joe* is passed as an argument to the function.it replaces the name parameter inside the function.

## Function Return values
Functions can return a value using the return keyword. This allows us to store and use the result later.
eg. 
function add(number1, number2) {
    return number1 + number2;
}

let sum = add(35, 23);
console.log(sum); // Outputs: 58
- he function returns the sum of number1 and number2, which is then stored in sum and printed.

## Categories of Functions
#### Functions That Don't Take Parameters and Don't Return a Value
These functions execute a task but don't require any input or provide a result.

eg. function greetUser() {
    console.log("Welcome to our website!");
}

greetUser();

### Functions That Don't Take Parameters but Return a Value
These functions return a result but don’t require input.
eg.
function getRandomNumber() {
    return Math.random();
}

console.log(getRandomNumber()); // Outputs a random number

### Functions That Take Parameters but Don't Return a Value
- These functions receive inputs and perform a task but don’t return a result.
eg. 
function displaySum(a, b) {
    console.log(`The sum of ${a} and ${b} is ${a + b}`);
}

displaySum(5, 3); // Outputs: The sum of 5 and 3 is 8


displaySum(5, 3); // Outputs: The sum of 5 and 3 is 8
### Functions that take Parameters and Return a Value
- These functions receive inputs and return a processed result.
eg. 
function multiply(a, b) {
    return a * b;
}

console.log(multiply(5, 3)); // Outputs: 15


## Types of Functions in JavaScript
### Function Declaration
A function defined using the function keyword.
eg. 
function subtract(a, b) {
    return a - b;
}

console.log(subtract(10, 3)); // Outputs: 7

console.log(subtract(10, 3)); // Outputs: 7
### Function Expression (Anonymous Function)
A function assigned to a variable without a name.
eg. 
let divide = function (a, b) {
    return a / b;
};

console.log(divide(10, 2)); // Outputs: 5

### Arrow Functions
Introduced in ES6, arrow functions provide a shorter syntax.
eg. 
let multiply = (a, b) => a * b;

console.log(multiply(5, 3)); // Outputs: 15

## Immediately Invoked Function Expressions (IIFE)
These functions execute immediately after being defined.
eg.
(function (a, b) {
    console.log(`The sum of ${a} and ${b} is ${a + b}`);
})(5, 6);

## Callback Functions
A callback function is a function passed as an argument to another function.
eg.
function greet(name, callback) {
    console.log(`Hello ${name}`);
    callback();
}

greet("Dennis", function () {
    console.log("Welcome back");
});
- the second argument is an anonymous function that executes after greet runs.