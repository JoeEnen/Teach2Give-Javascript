# Control flow
- It is the manner/order in which instructions and statements are executed in a program.
- Normally, js runs the code from to to bottom. However, control flow allows us to alter this execution.
- Control flow is achieved using: 
. conditional
. loops

## Conditional
- this allows different code blocks to be executed based on specified conditions.
- common conditional statements:
. if statement
. if else statement
. if else ladder
. switch statement

### if statements:
-Only work if a condition is true.
eg. 
let age= 50
if (age > 18) {
  console.log("You are an adult");
}
### if else statement
- the code is executed if the condition is true. If not, the code inside the else block is executed.
eg.
let age= 17
if (age > 18) {
  console.log("You are an adult");
} else {
  console.log("You are a child");
}
### if else ladder
-Applicable is several conditions must be checked sequentially.
eg. 
let marks = 60;
if (marks >= 88) {
  console.log("Grade: A");
} else if (marks >= 80 && marks < 88) {
  console.log("Grade: B");
} else if (marks >= 70 && marks < 80) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
### Switch statement
-Applicable if a variable has multiple possible values. 
eg. 
let day = "Sunday";
switch (day) {
  case "Sunday":
    console.log("Resting day.");
    break;
  case "Friday":
    console.log("Weekend is near!");
    break;
  case "Monday":
    console.log("Start of the week.");
    break;
  default:
    console.log("It's a regular day.");
}
### Ternary Operator
-They provide a simpler way of writing the "if-else statements" in a single line.
eg.
const marks = 30;

age > 25 ? console.log("You passed exam") : console.log("You failed exam");
