## How does Node.js handle I/O operations efficiently?

---

Node js handle I/O operations by Using :

-Non-blocking I/O
-Event-driven architecture
-Event Loop
-libuv + Thread Pool

Instead of waiting for an I/O operation like a file read, database query, or network request to finish, Node.js continues executing other tasks.


### Simple Example

```js
const fs = require("fs");

console.log("Start");

fs.readFile("data.txt", "utf8", (err, data) => {
  console.log(data);
});

console.log("End");