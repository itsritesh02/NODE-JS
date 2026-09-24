## What are Callback, Promise, and Async/Await?

---

Callbacks, Promises, and Async/Await are different ways to handle asynchronous operations in JavaScript.

## 1. Callback

A callback is a function passed as an argument to another function.
It is executed after the asynchronous operation is completed.

Example:

function getData(callback) {
  setTimeout(() => {
    callback("Data received");
  }, 1000);
}

getData((data) => {
  console.log(data);
});

Output:
Data received

Callbacks can become difficult to manage when there are many nested callbacks.
This is called Callback Hell.

---

## 2. Promise

A Promise represents the future result of an asynchronous operation.

A Promise has three states:

Pending
   ↓
Fulfilled
   OR
Rejected

Example:

function getData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Data received");
    }, 1000);
  });
}

getData()
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });

Important:

resolve() → Success
reject()  → Failure
.then()   → Handles success
.catch()  → Handles error

---

## 3. Async/Await

Async/Await is a cleaner and more readable way to work with Promises.

- async makes a function return a Promise.
- await waits for the Promise result inside an async function.

Example:

function getData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data received");
    }, 1000);
  });
}

async function fetchData() {
  try {
    const data = await getData();

    console.log(data);
  } catch (error) {
    console.log(error);
  }
}

fetchData();

Output:
Data received

---

## Difference Between Callback, Promise, and Async/Await

Callback:
- Uses a callback function
- Can become nested
- Can lead to Callback Hell

Promise:
- Uses resolve and reject
- Uses .then() and .catch()
- Easier to manage asynchronous operations

Async/Await:
- Works with Promises
- Uses try/catch for error handling
- Cleaner and easier to read

---

## Simple Flow

Callback:
Function → Callback → Result

Promise:
Function → Promise → .then() / .catch() → Result

Async/Await:
Function → Promise → await → Result

---

## Interview Answer

"Callbacks, Promises, and Async/Await are ways to handle asynchronous operations in JavaScript. A callback is a function executed after an operation completes. A Promise represents the future result of an asynchronous operation and can be handled using then and catch. Async/Await provides a cleaner and more readable way to work with Promises."