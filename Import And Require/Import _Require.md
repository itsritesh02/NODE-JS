## What is the Difference Between `import` and `require`?

Both `import` and `require` are used to load and reuse modules or packages in Node.js.

The main difference is that `require` is used with the CommonJS module system, while `import` is used with the ES Module system.

In CommonJS, we use `require()` for importing and `module.exports` for exporting.

### Example:

const express = require('express');

In ES Modules, we use `import` and `export`:

import express from 'express';

So, the main difference is the module system and syntax they use.

Node.js supports both CommonJS and ES Modules.

---

### Simple Definition

```text
require() → CommonJS module system

import    → ES Module system