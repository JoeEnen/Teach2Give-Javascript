# Abstraction
- Abstraction is an OOP principle that focuses on hiding implementation details while exposing only the necessary functionality. This simplifies interactions with objects by providing a clean and easy-to-use interface.

## Difference Between Abstraction and Encapsulation
. Encapsulation- Hides data and restricts access using private fields (#)
. Abstraction- Hides implementation details, exposing only necessary methods

# Implementing Abstraction in JavaScript
- Using private fields (#) and public methods to control access:

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

  withdraw(amount) {
    if (amount > this.#balance) {
      console.log("Insufficient balance!");
    } else {
      this.#balance -= amount;
      console.log(`Withdrew ${amount}. New balance: ${this.#balance}`);
    }
  }
}

// Creating an instance
const account = new BankAccount("John");

account.deposit(500);
account.withdraw(900); // X Insufficient balance!
account.withdraw(200); // ✅ Withdrew 200. New balance: 300

*How Abstraction Works Here:*
✔ User only interacts with deposit(), withdraw(), and checkBalance()
✔ The logic behind #balance is hidden
✔ Internal calculations and validations are abstracted away


