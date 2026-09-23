## What is Event Loop?

---

The **Event Loop** is a mechanism that allows Node.js to perform **non-blocking asynchronous operations** using a single JavaScript thread.

It continuously checks:

- Is the **Call Stack** empty?
- Are there any **pending callbacks or asynchronous tasks**?

If the Call Stack is empty, the Event Loop moves the ready callbacks to the Call Stack for execution.

This is why Node.js can handle many concurrent requests efficiently without creating a new JavaScript thread for each request.

### Simple Example

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

console.log("End");