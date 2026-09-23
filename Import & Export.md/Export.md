# Difference Between module.exports and export

---

`module.exports` and `export` are used to export data from a file, but they belong to different module systems.

## 1. module.exports

`module.exports` is used in the **CommonJS** module system.

    // user.js

    const name = "Ritesh";

    module.exports = name;

    // app.js

    const name = require("./user");

    console.log(name);


## 2. export

`export` is used in the **ES Module (ESM)** system.

    // user.js

    const name = "Ritesh";

    export default name;

    // app.js

    import name from "./user.js";

    console.log(name);


## Main Difference

| module.exports | export |
|---|---|
| CommonJS | ES Modules (ESM) |
| Uses `require()` | Uses `import` |
| `module.exports` | `export` / `export default` |
| Common in older Node.js code | Modern JavaScript |
| `const data = require()` | `import data from` |

## Multiple Exports

### CommonJS

    module.exports = {
      name: "Ritesh",
      age: 22
    };

    const { name, age } = require("./user");


### ES Module

    export const name = "Ritesh";
    export const age = 22;

    import { name, age } from "./user.js";


## Interview Answer

`module.exports` is part of the CommonJS module system and is generally used with `require()`, while `export` is part of the ES Module system and is used with `import`. In modern JavaScript and Node.js projects, ES Modules are commonly used.