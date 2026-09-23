## What is FS Module?

---

The **FS (File System) module** is a built-in Node.js module used to **work with files and directories**.

It allows us to:

- Create files
- Read files
- Write files
- Update files
- Delete files
- Create and remove directories

### Simple Example

```js
const fs = require("fs");

// Write data to a file
fs.writeFile("data.txt", "Hello Ritesh", (err) => {
  if (err) {
    console.log(err);
    return;
  }

  console.log("File created successfully");
});

// Read data from the file
fs.readFile("data.txt", "utf8", (err, data) => {
  if (err) {
    console.log(err);
    return;
  }

  console.log(data);
});