# Promises
- A Promise is an object that represents the eventual completion (or failure) of an asynchronous operation. It provides a better way to handle async code compared to callbacks.

## Why Use Promises?
- When dealing with asynchronous JavaScript, there are two types of code:

1 Producing Code – Takes time to complete (e.g., fetching user data from an API).
2 Consuming Code – Waits for the result from the producing code.

- A promise links producing and consuming code, allowing structured handling of async operations.

## Promise States
Pending- Initial state; operation not yet completed.
Fulfilled- Operation completed successfully.
Rejected- Operation failed.

## Creating a Promise
- A Promise is created using new Promise(), which takes an executor function with two parameters:

. resolve(value): Called when the operation succeeds.
. reject(error): Called when the operation fails.

let myPromise = new Promise(function (resolve, reject) {
  let x = 1;
  if (x === 1) {
    resolve("x is 1"); // Success
  } else {
    reject("x is not 1"); // Failure
  }
});

## Consuming a Promise
We use:

.then(callback) – Runs when the Promise resolves successfully.
.catch(callback) – Runs when the Promise rejects (fails).

myPromise
  .then((result) => {
    console.log(result); // "x is 1"
  })
  .catch((error) => {
    console.log(error); // "x is not 1"
  });

.finally() – Runs Regardless of Success or Failure
The .finally() method executes after either then() or catch(), useful for cleanup tasks.

 myPromise
  .then((result) => console.log(result))
  .catch((error) => console.log(error))
  .finally(() => console.log("It was nice working with this promise"));

  ##  Returning a Promise from a Function
- A function can return a Promise to handle async operations more effectively.

function fetchUser() {
  return new Promise((resolve, reject) => {
    let error = false;
    if (error) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

fetchUser()
  .then((user) => {
    console.log(`Username: ${user.username}, Role: ${user.role}`);
  })
  .catch((error) => {
    console.log(error);
  });

