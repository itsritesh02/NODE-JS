# What are Built-in Modules in Node.js?

---

Built-in modules are modules that are already provided by Node.js.

We don't need to install them using npm.

## Examples

- `fs` → File system
- `http` → Create HTTP server
- `path` → Work with file paths
- `os` → Get operating system information

## Example

    const fs = require("fs");

    fs.readFile("data.txt", "utf8", (err, data) => {
      console.log(data);
    });

## Interview Answer

"Built-in modules are modules already provided by Node.js. We don't need to install them. For example, fs, http, path, and os."