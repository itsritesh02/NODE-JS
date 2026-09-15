const http = require("http");
const EventEmitter = require("events");
const fs = require("fs");

// =====================================================
// 1. SINGLE-THREADED
// =====================================================

// Node.js executes JavaScript code on a single main thread.
// The Event Loop helps this thread handle multiple tasks.

console.log("Task 1");
console.log("Task 2");
console.log("Task 3");

// Output:
// Task 1
// Task 2
// Task 3

// Interview:
// "Node.js uses a single main thread to execute JavaScript code.
// The Event Loop helps it handle multiple operations efficiently."


// =====================================================
// 2. ASYNCHRONOUS
// =====================================================

// Node.js does not wait for the file operation to finish.
// It starts the file operation and continues executing other code.

fs.readFile("data.txt", "utf8", (err, data) => {
    console.log("File operation completed");
});

console.log("Other work continues");

// Possible Output:
// Other work continues
// File operation completed

// Interview:
// "Node.js is asynchronous, which means it can start a time-consuming
// operation and continue executing other code without waiting for it to finish."


// =====================================================
// 3. EVENT-DRIVEN
// =====================================================

// Node.js works with events.
// When an event occurs, its registered handler is executed.

const event = new EventEmitter();

// Event listener
event.on("login", () => {
    console.log("User logged in");
});

// Trigger the event
event.emit("login");

// Output:
// User logged in

// What happens?
// on()    -> listens for an event
// emit()  -> triggers the event
//
// Interview:
// "Node.js follows an event-driven architecture where actions are
// performed when specific events occur."


// =====================================================
// 4. V8 JAVASCRIPT ENGINE
// =====================================================

// Node.js uses Google's V8 JavaScript engine
// to execute JavaScript code.

const name = "Ritesh";

console.log(name);

// V8 is responsible for executing JavaScript.
//
// Interview:
// "Node.js uses Google's V8 JavaScript engine to execute JavaScript.
// V8 converts JavaScript into optimized machine code for execution."


// =====================================================
// 5. CROSS-PLATFORM
// =====================================================

// Node.js applications can run on different operating systems
// such as Windows, Linux and macOS.

console.log(process.platform);

// Example output on Windows:
// win32
//
// Linux:
// linux
//
// macOS:
// darwin
//
// Interview:
// "Node.js is cross-platform, which means the same Node.js
// application can run on Windows, Linux and macOS."


// =====================================================
// 6. NPM
// =====================================================

// NPM = Node Package Manager
//
// It is used to install and manage packages.
//
// Example:
// npm install express
//
// After installation:
//
// const express = require("express");
//
// NPM provides thousands of reusable packages.
//
// Examples:
// Express
// Mongoose
// Bcrypt
// JWT
// Multer
//
// Interview:
// "NPM stands for Node Package Manager. It is used to install,
// manage and share reusable packages in Node.js applications."


// =====================================================
// 7. REAL-TIME CAPABILITIES
// =====================================================

// Node.js is suitable for applications where users
// need updates with very low delay.
//
// Examples:
// Chat applications
// Live notifications
// Online gaming
// Live tracking
//
// Real-time applications commonly use WebSockets or Socket.IO.
//
// Example concept:
//
// User A  <------>  Server  <------>  User B
//
// Message sent by User A
//        ↓
// Server receives it
//        ↓
// User B receives it immediately


// =====================================================
// SIMPLE NODE SERVER
// =====================================================

const server = http.createServer((req, res) => {
    res.end("Hello Node.js");
});

server.listen(5000, () => {
    console.log("Server running on port 5000");
});