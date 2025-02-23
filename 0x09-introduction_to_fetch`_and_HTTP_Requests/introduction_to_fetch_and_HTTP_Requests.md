# Introduction to fetch and HTTP Requests
- The fetch function is a built-in JavaScript method that enables communication with servers over the internet. It allows your code to send and receive data from APIs (Application Programming Interfaces).

## What is fetch?
- Think of fetch like asking a friend for information:

1.You ask: "Hey, what's the weather today?"
2.They respond: "It’s sunny and 25°C."

- Similarly, fetch sends a request to a server, and the server responds with some data.

## HTTP Requests
- HTTP (HyperText Transfer Protocol) is how computers communicate over the web.

- There are different types of HTTP requests:
Request Type>	Description> Example

GET> Requests data from a server> "Give me a list of users"
POST> Sends data to create something> "Create a new user"
PUT> Updates existing data> "Change John's name to Jack"
DELETE> Removes data from the server> "Delete John's account"

## Making a Simple fetch Request (GET Request)
- getting fake user data from a free API:

fetch("https://jsonplaceholder.typicode.com/users")
  .then(function (response) {
    return response.json(); // Convert response to JSON
  })
  .then(function (data) {
    console.log(data); // Display user data
  })
  .catch(function (error) {
    console.log("There was an error");
    console.log(error);
  });

*How This Works:*
fetch("https://jsonplaceholder.typicode.com/users") → Sends a GET request to the server.
.then(response => response.json()) → Converts the server response into JSON format.
.then(data => console.log(data)) → Displays the data in the console.
.catch(error => console.log(error)) → Handles errors (e.g., no internet connection).

## Using Async/Await for Simplicity
- Instead of .then(), we can use async/await for cleaner code:

async function fetchUser() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users/1");
    const data = await response.json(); // Convert response to JSON
    console.log(data); // Display user data
  } catch (error) {
    console.error("Error:", error); // Handle errors
  }
}

fetchUser();

*Why Use Async/Await?*
1 More readable
2 Easier to debug
3 Looks like synchronous code but is still asynchronous

## Handling Errors Properly
- When working with fetch, things can go wrong (e.g., server issues, no internet). Always handle errors:

async function fetchUser() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users/1");

    if (!response.ok) {
      console.log("Something went wrong"); // Checks for failed request
      return;
    }

    const data = await response.json(); // Convert response to JSON
    console.log(data); // Display user data
  } catch (error) {
    console.error("Error:", error); // Handles network errors
  }
}

fetchUser();

