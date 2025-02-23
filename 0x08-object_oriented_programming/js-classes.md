# Object-Oriented Programming (OOP)
 - is a programming paradigm based on the concept of objects, which bundle data (properties) and behaviors (methods) together.
- It promotes code reusability, modularity, and scalability.
## JavaScript Classes (ES6)
Before ES6 (2015), JavaScript relied on constructor functions for object-oriented programming (OOP). ES6 introduced the class syntax, making OOP more structured and readable.

### What is a Class?
A class is a blueprint for creating objects. It defines properties (data) and methods (functions) that objects will have.

### Creating a Class in JavaScript
Use the class keyword, followed by a class name. The constructor method initializes object properties.

class User {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`My name is ${this.name}`);
  }
}

1. constructor(name, age) initializes properties (name and age).
2. greet() is a method inside the class.

### Creating an Instance of a Class
- Use the new keyword to create an object (instance) from the class.

const user1 = new User("John Doe", 25);
user1.greet(); // Output: My name is John Doe

