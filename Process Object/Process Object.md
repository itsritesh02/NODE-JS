## What is Process Object?

---

The **process object** is a global object in Node.js that provides information about and control over the **current Node.js process**.

We can use it to access:

- Environment variables
- Process ID
- Node.js version
- Command-line arguments
- Exit the process

### Simple Example

```js
console.log(process.pid);
console.log(process.version);
console.log(process.env);