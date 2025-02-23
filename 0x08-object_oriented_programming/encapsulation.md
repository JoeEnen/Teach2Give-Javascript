# Encapsulation in JavaScript
- Encapsulation is an OOP principle that involves bundling data (properties) and methods (functions) into a single unit (object) while restricting direct access to some details.

## Why Use Encapsulation?
✔ Prevents direct modification of data
✔ Ensures controlled access through methods
✔ Improves security and maintainability

## Encapsulation Using Private Fields (#)
- In ES6, we use the # symbol to define private properties inside a class.

class BankAccount {
  #balance = 0; // Private property

  constructor(owner) {
    this.owner = owner;
  }

  deposit(amount) {
    this.#balance += amount;
    console.log(`Deposited ${amount}. New balance: ${this.#balance}`);
  }

  checkBalance() {
    console.log(`Current balance: ${this.#balance}`);
  }
}

const account = new BankAccount("John");
account.deposit(500);
account.checkBalance();

// console.log(account.#balance); // ❌ Error: Private field '#balance' must be declared

*How Encapsulation Works Here:*
. #balance is private → Cannot be accessed directly from outside.
. Methods (deposit(), checkBalance()) allow controlled interaction with #balance.
. Prevents accidental modification of sensitive data.

## Encapsulation Using Getters and Setters
We can use getter (get) and setter (set) methods to safely retrieve and modify private properties.
class User {
  #password;

  constructor(username, password) {
    this.username = username;
    this.#password = password;
  }

  get password() {
    return "Access denied!"; // Prevents direct access
  }

  set password(newPassword) {
    if (newPassword.length < 6) {
      console.log("Password must be at least 6 characters!");
    } else {
      this.#password = newPassword;
      console.log("Password updated successfully!");
    }
  }
}

const user = new User("john_doe", "123456");
console.log(user.password); // "Access denied!"
user.password = "pass"; // "Password must be at least 6 characters!"
user.password = "newPassword"; // "Password updated successfully!"

## Why Encapsulation is Important?

. Prevents accidental modifications of sensitive data.
. Improves security by restricting direct access.
. Encourages better design with controlled interactions.