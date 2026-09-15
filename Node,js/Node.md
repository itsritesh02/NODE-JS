## What is Node JS?

---

Node js is Neither a language nor a frameWork.
Its a runtime Enviroment for executing javascript code on the  server side.

built on Chrome's V8 JavaScript engine

---

### Example

---
const http = require("http");

const server = http.createServer((req, res) => {
  res.end("Hello from Node.js");
});

server.listen(5000, () => {
  console.log("Server is running on port 5000");
});


** Q1. Why is Node.js fast? **
→ V8 engine + non-blocking asynchronous I/O.

** Q4. Why use Node.js for backend? **
→ Fast development, JavaScript across frontend/backend, non-blocking I/O, and good suitability for I/O-heavy applications.