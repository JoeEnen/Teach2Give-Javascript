# Loops
- Allows executions of a block f code repeatedly.
- Basic loops; for loop. while loop and do while loop
# Types
a. for loop – when the number of iterations is known
b. while loop – Runs as long as a specified condition remains true
c. do while loop – Executes at least once, even if the condition is false initially

## for Loop
- used when we know how many times a block of code should run.

for (initialization; condition; update) {
    // code to execute
}
- Initialization: Sets up the loop variable.
- Condition: Determines whether the loop continues running.
- Update: Modifies the loop variable after each iteration.

## while Loop
- The while loop continues running as long as a specified condition remains true.
eg.
let num = 3;

while (num <= 5) {
    console.log("Number ", num);
    num++;
}

## do while Loop
The do while loop guarantees that the code block will run at least once, even if the condition is false at the start.
eg. 
let x = 2;

do {
    console.log("x ", x);
    x++;
} while (x <= 5);

Break and Continue Statements
The break Statement
The break statement is used when we need to exit a loop completely before it naturally finishes.

Example:
js
Copy
Edit
for (let i = 0; i < 10; i++) {
    if (i == 5) {
        break; // *Stops the loop when i equals 5*
    }
    console.log(i);
}
Once i reaches 5, the loop stops executing.

# break Statement
_ The break statement is used when we need to exit a loop completely before it naturally finishes.
eg. 
for (let i = 0; i < 10; i++) {
    if (i == 5) {
        break; // Stops the loop when i equals 5
    }
    console.log(i);
}
- Once i reaches 5, the loop stops executing.

# continue Statement
- The continue statement is used when we need to skip a specific iteration but allow the loop to continue running.

example:
for (let i = 0; i < 10; i++) {
    if (i == 5) {
        continue; // *Skips iteration when i is 5*
    }
    console.log(i);
}
- When i is 5, the loop skips that iteration but continues with the remaining values.