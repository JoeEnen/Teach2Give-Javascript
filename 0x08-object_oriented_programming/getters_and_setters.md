# Getters and Setters in JavaScript
- Getters and Setters are special methods used to control access to an object's properties. They help in data encapsulation, preventing direct modification of properties while allowing validation and control.

## Why Use Getters and Setters?
-Encapsulation – Restricts direct access to properties.
-Validation – Ensures data integrity before updating values.
-Code Readability – Allows clean, controlled access to properties.

## Example Without Getters and Setters (Direct Access Issue)
class User {
  constructor(name) {
    this.name = name; // Direct access (No validation)
  }
}

const user = new User("Dennis");
console.log(user.name); // "Dennis"

user.name = 42; // ❌ No validation, allows invalid data
console.log(user.name); // 42 (Not ideal)

❌ No control over the name property.
❌ Invalid values like numbers can be assigned.

## 3. Using Getters and Setters (Controlled Access)
class User {
  constructor(name) {
    this._name = name; // Private property convention (_name)
  }

  // Getter (retrieves the value)
  get name() {
    return this._name;
  }

  // Setter (validates before updating)
  set name(newName) {
    if (typeof newName !== "string") {
      console.error("Name must be a string!");
      return;
    }
    this._name = newName;
  }
}

const user = new User("Dennis");

// Using the getter
console.log(user.name); // "Dennis"

// Using the setter
user.name = "John"; // ✅ Updates successfully
console.log(user.name); // "John"

user.name = 42; // ❌ Error: Name must be a string!

