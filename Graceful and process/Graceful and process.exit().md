## process.exit() vs Graceful Shutdown

---

Both `process.exit()` and **graceful shutdown** are used to stop a Node.js application.

The main difference is:

- `process.exit()` → Immediately stops the Node.js process.
- Graceful Shutdown → Properly closes the server and resources before stopping the process.

### Simple Example

```js
const express = require("express");

const app = express();

const server = app.listen(5000, () => {
  console.log("Server is running on port 5000");
});

/*
=================================================
GRACEFUL SHUTDOWN
=================================================

Graceful shutdown means properly shutting down
the application.

Before exiting, we:
1. Stop accepting new requests.
2. Complete pending requests.
3. Close the server.
4. Close database connections and other resources.
5. Exit the process.
*/

process.on("SIGTERM", () => {
  console.log("Shutdown signal received");

  server.close(() => {
    console.log("Server closed");

    // Exit after cleanup is completed
    process.exit(0);
  });
});

/*
=================================================
FORCEFUL SHUTDOWN
=================================================

process.exit() immediately terminates the process.

It does not wait for pending operations to finish.
*/

function forceShutdown() {
  console.log("Forcefully shutting down...");

  process.exit(1);
}