# What is a Module in Node.js?

A module is a reusable block of code that can be exported and imported in other files.

## Example

    // math.js

    const add = (a, b) => {
      return a + b;
    };

    module.exports = add;


    // app.js

    const add = require("./math");

    console.log(add(10, 20));
