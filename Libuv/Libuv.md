## What is libuv?

---

**libuv** is a **C library used by Node.js** to handle asynchronous and non-blocking operations.

It helps Node.js handle tasks such as:

- Event Loop
- Asynchronus I/O
- Thread Pool
- Timers
- File System & networking


javaScript alone can't do async I/O efficiently-libuv makes Node.js fast

### Simple Example

```js
const fs = require("fs");

console.log("Start");

fs.readFile("data.txt", "utf8", (err, data) => {
  console.log(data);
});

console.log("End");