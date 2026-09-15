# Import and Export in JavaScript

`import` and `export` are used to share and use code between different files.

---

## Types of Import and Export

There are mainly **2 types**:

### 1. Named Export / Import

Named export is used when we want to export multiple variables, functions, or components.

**user.js**

```js
export const name = "Ritesh";

export const age = 22;



import { name, age } from "./user.js";

console.log(name);

console.log(age);



### 2 Default Export — Definition

Default Export is used to export one main value, function, or component from a file.

### Simple Definition

Default Export → One default value can be exported from a file.

## Default Export — Example

### user.js

```js
const name = "Ritesh";

export default name;

import name from "./user.js";

console.log(name);