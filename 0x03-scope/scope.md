# Scope
-scope determines where variables can be accessed in a program. It defines whether a variable is visible inside or outside a function or block.
- types
1. Global Scope
2. Function Scope (Local Scope)
3. Block Scope (introduced in ES6)
3. Lexical Scope

## Global scope
- are variables declared outside any function or block. This means they are is accessible anywhere in the JS program.
eg. 
let age = 25; *Global variable*

function exampleFunction() {
    console.log(age); *Accessible inside function*
}

exampleFunction(); *Output: 25*
console.log(age); *Output: 25 (Accessible outside function too)*
- age is accessible both inside and outside the function because it was declared in the global scop
## Function Scope (Local Scope)
_ a variable declared inside a function is only accessible within that function. It cannot be accessed outside the function.
eg. 
function exampleFunction() {
    let age = 25; *Function-scoped variable*
    console.log(age); *Works inside the function*
}

exampleFunction();
console.log(age); *ReferenceError: age is not defined*
- Since age is declared inside exampleFunction(), it cannot be accessed outside the function.
##  Block Scope (let and const)
- Before ES6, JavaScript only had global scope and function scope. The var keyword did not support block scope.

- However, ES6 introduced let and const, which have block scope. A block is any code inside curly brackets {} (e.g., inside if, for, or while statements).
 eg. 
 if (true) {
    let age = 25;
    console.log(age); *Works inside the block*
}
console.log(age); *ReferenceError: age is not defined*

- Variables declared with let and const are only accessible inside the block they are declared in.
- However, var does not follow block scope:
 eg. 
 if (true) {
    var age = 25;
}
console.log(age); *Output: 25 (accessible outside the block)*

-Because var is not block-scoped, it is accessible outside the if statement.

## Lexical Scope
- Lexical Scope means that a function can access variables from its parent function or parent scope.
eg.
 function parentFunction() {
    let age = 25;

    function innerFunction() {
        console.log(age); *Accesses 'age' from parentFunction*
    }

    innerFunction();
}

parentFunction(); *Output: 25*

- Here, innerFunction() does not have its own age variable, but it can access the age variable from parentFunction() because of lexical scope.



