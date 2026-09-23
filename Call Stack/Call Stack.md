## What is Call Stack?

---

The **Call Stack** is a data structure used by JavaScript to keep track of **function calls**.

It follows the **LIFO (Last In, First Out)** principle.

Only Synchronus code goes into Call Stack

When a function is called, it is added to the Call Stack.  
When the function finishes execution, it is removed from the Call Stack.

### Simple Example

```js
function first() {
  console.log("First");
}

function second() {
  first();
  console.log("Second");
}

second();