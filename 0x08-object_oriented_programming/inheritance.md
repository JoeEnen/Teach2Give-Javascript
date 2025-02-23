# Inheritance in JavaScript
- Inheritance is an OOP principle that allows one class to inherit properties and methods from another class. This promotes code reusability and hierarchical structuring of objects.
 *Why Use Inheritance?*
1 Avoids code duplication – Common behavior is defined once and reused.
2 Creates a logical structure – e.g., A Dog is an Animal, a Car is a Vehicle.
3 Enhances maintainability – Changes in the parent class apply to all child classes.

2. Implementing Inheritance in JavaScript
- Using the extends keyword, a child class can inherit from a parent class.
Example: Vehicle & Car
 
 // Parent class
class Vehicle {
  constructor(brand, wheels) {
    this.brand = brand;
    this.wheels = wheels;
  }

  drive() {
    console.log(`${this.brand} is driving on ${this.wheels} wheels.`);
  }
}

// Child class inheriting from Vehicle
class Car extends Vehicle {
  constructor(brand, wheels, model) {
    super(brand, wheels); // Calls parent constructor
    this.model = model;
  }

  honk() {
    console.log(`${this.brand} ${this.model} is honking!`);
  }
}

// Creating an instance of Car
const myCar = new Car("Toyota", 4, "Corolla");

myCar.drive(); // Toyota is driving on 4 wheels.
myCar.honk();  // Toyota Corolla is honking!

*How Inheritance Works Here:*
✔ Car extends Vehicle → It inherits drive().
✔ super() calls the parent constructor to set properties.
✔ Car has its own method (honk()), in addition to inherited methods.
