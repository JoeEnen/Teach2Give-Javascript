# Polymorphism in JavaScript
- Polymorphism is an OOP principle that allows methods to have multiple forms, meaning the same method can behave differently in different contexts.

## Types of Polymorphism
- Method Overriding – A child class provides its own version of an inherited method.
- Method Overloading – A method with the same name but different parameters (not natively supported in JavaScript but can be simulated).

### Method Overriding in JavaScript
- When a subclass (child class) defines a method with the same name as a method in the parent class, but with a different implementation.

Example: Animal Sounds
// Parent class
class Animal {
  makeSound() {
    console.log("Some generic animal sound...");
  }
}

// Child class 1
class Dog extends Animal {
  makeSound() {
    console.log("Woof! Woof!");
  }
}

// Child class 2
class Cat extends Animal {
  makeSound() {
    console.log("Meow! Meow!");
  }
}

const myDog = new Dog();
const myCat = new Cat();

myDog.makeSound(); // Woof! Woof!
myCat.makeSound(); // Meow! Meow!

- *makeSound()* behaves differently depending on the object (Dog or Cat).
- The child class overrides the parent’s method to provide a specific behavior.

### Method Overloading (Simulated in JavaScript)
- JavaScript does not support method overloading like other languages (Java, C++). However, it can be simulated using default parameters or argument checks.

Example: Simulating Overloading in JavaScript

class MathOperations {
  add(number1, number2, number3 = 0) {
    return number1 + number2 + number3;
  }
}

const math = new MathOperations();
console.log(math.add(5, 10));     // 15
console.log(math.add(5, 10, 15)); // 30

✔ Same method name (add) but handles different numbers of arguments.
✔ Uses default values (number3 = 0) to simulate overloading.
