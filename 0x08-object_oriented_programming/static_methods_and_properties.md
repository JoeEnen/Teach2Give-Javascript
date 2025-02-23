# Static Methods and Properties in JavaScript
- Static methods and static properties belong to a class itself, not its instances. This means they can be accessed directly from the class without creating an object.

## Static Methods
- A static method is defined using the static keyword and can only be called on the class itself, not on instances.

Example: Math Utility Class
class MathUtils {
  static add(a, b) {
    return a + b;
  }

  static subtract(a, b) {
    return a - b;
  }
}

// Calling static methods directly from the class
console.log(MathUtils.add(10, 5));      // 15
console.log(MathUtils.subtract(10, 5)); // 5

// Trying to call a static method on an instance (❌ Error)
// const math = new MathUtils();
// console.log(math.add(10, 5)); // TypeError: math.add is not a function

## Static Properties
- A static property is a variable that belongs to the class itself instead of individual objects.

Example: Counter Class
class Counter {
  static count = 0; // Static property

  static increment() {
    Counter.count++;
  }

  static getCount() {
    return Counter.count;
  }
}

// Accessing static property without creating an instance
console.log(Counter.getCount()); // 0

Counter.increment();
Counter.increment();

console.log(Counter.getCount()); // 2
