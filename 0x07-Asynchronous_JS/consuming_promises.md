# Consuming Promises with Async/Await
- The async/await syntax provides a modern, cleaner way to handle asynchronous operations in JavaScript. It is built on Promises but allows writing asynchronous code that looks synchronous, improving readability.

## Using Async/Await to Consume a Promise
A function that returns a Promise:

function fetchUser() {
  return new Promise((resolve, reject) => {
    let error = false; // Change to true to simulate failure
    if (error) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

*Using async/await to handle the Promise:*

async function processUser() {
  const user = await fetchUser();
  console.log(user);
}

processUser();

## Handling Errors with Try...Catch
To prevent crashes, use try...catch to handle errors gracefully:

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch {
    console.log("An error occurred");
  }
}

processUser();

## Capturing Errors with *Try* Catch and Error Parameter
- The catch block can receive the error message from the rejected Promise:

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch (error) {
    console.log(error); // Logs "There was an error"
  }
}

processUser();

## Using Finally Block
- The finally block executes regardless of success or failure (useful for cleanup operations):
- this method ensures that some code runs no matter what happens.

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch (error) {
    console.log(error);
  } finally {
    console.log("Process completed");
  }
}

processUser();



