# Asynchronous JavaScript
- Asynchronous JavaScript refers to the execution of JavaScript without blocking the main thread, allowing other operations to continue while waiting for other tasks to complete.

## Callbacks
- Callbacks are a solution for handling asynchronous operations in JavaScript. They ensure that a function executes only after an operation is complete.

## Why Use Callbacks?
- Consider a function that fetches user data synchronously:

function fetchData() {
    let data = { username: "John Doe", role: "Admin" };
    return data;
}

function showData(data) {
    console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);

## Handling Asynchronous Code with Callbacks
- If fetching data takes time (e.g., from an API), the function will return undefined before the data is ready:
function fetchData() {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    return data; // This does not wait for execution
  }, 2000);
}

const userData = fetchData();
showData(userData); *❌ userData is undefined*

*Solution: use callbacks*

function fetchData(callback) {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    callback(data);
  }, 2000);
}

fetchData(function (data) {
  console.log(`Username is ${data.username} and role is ${data.role}`);
});

## Callback Hell (Deep Nesting Problem)
- Fetching user data, posts, and comments using callbacks:

fetchUser((user) => {
  fetchPosts(user, (posts) => {
    fetchComments(posts[0], (comments) => {
      console.log(`User: ${user.username}, Role: ${user.role}`);
      console.log(`Posts: ${posts}`);
      console.log(`Comments on first post: ${comments}`);
    });
  });
});

- Problems with Nested Callbacks:
1 Hard to read (deep indentation)
2 Difficult to debug
3 Scales poorly

## Better Alternative: Use Promises
- Promises help avoid callback hell by making asynchronous code more readable.

fetchUser()
  .then(user => fetchPosts(user))
  .then(posts => fetchComments(posts[0]))
  .then(comments => {
    console.log("User data, posts, and comments fetched successfully!");
  })
  .catch(error => console.log(error));

- Benefits
. Cleaner structure
. Easier debugging
. Better error handling