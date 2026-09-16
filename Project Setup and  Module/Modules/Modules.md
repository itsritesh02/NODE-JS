# Top 5 Built-in Modules in Node.js

## 1. `fs` — File System

Used to **read, write, update, and delete files**.

### Example

```js
const fs = require("fs");

fs.writeFileSync("hello.txt", "Hello Node.js");

const data = fs.readFileSync("hello.txt", "utf-8");

console.log(data);
```

**Interview:**  
`fs` module is used to work with files and directories in Node.js.

---

## 2. `http` — HTTP Server

Used to **create an HTTP server** and handle requests/responses.

### Example

```js
const http = require("http");

const server = http.createServer((req, res) => {
  res.end("Hello from Node.js");
});

server.listen(5000, () => {
  console.log("Server is running on port 5000");
});
```

**Interview:**  
`http` module is used to create HTTP servers and handle client requests and responses.

---

## 3. `path` — File Paths

Used to **work with file and directory paths**.

### Example

```js
const path = require("path");

const filePath = path.join("users", "ritesh", "data.txt");

console.log(filePath);
```

**Interview:**  
`path` module provides utilities for working with file and directory paths.

---

## 4. `os` — Operating System

Used to get **information about the operating system**.

### Example

```js
const os = require("os");

console.log(os.platform());
console.log(os.cpus().length);
console.log(os.totalmem());
```

**Interview:**  
`os` module is used to get information about the operating system and system resources.

---

## 5. `events` — Event Handling

Used to **create and handle custom events**.

### Example

```js
const EventEmitter = require("events");

const event = new EventEmitter();

event.on("login", () => {
  console.log("User logged in");
});

event.emit("login");
```

**Interview:**  
`events` module is used to create, handle, and emit custom events in Node.js.