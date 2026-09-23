## What is Blocking Code?

---

**Blocking code** is code that **stops the execution of the program until the current operation is completed**.

In Node.js, blocking operations can stop the main thread from handling other requests.

### Simple Example

```js
const fs = require("fs");

console.log("Start");

const data = fs.readFileSync("data.txt", "utf8");

console.log(data);

console.log("End");