# Unhandled Promise Rejection in Node.js Express App

This example demonstrates a common error in Node.js applications involving unhandled promise rejections or exceptions within asynchronous callbacks.  The Express.js server simulates an asynchronous operation that might fail. If the operation fails, an error is thrown, leading to an unhandled promise rejection if not properly caught. 

## Bug
The `bug.js` file contains an Express.js server with an asynchronous route handler.  The handler simulates an asynchronous operation that can either succeed or fail randomly. If it fails, an error is thrown without proper handling, resulting in a crash or unhandled rejection.

## Solution
The `bugSolution.js` file provides a corrected version. It uses a `try...catch` block to handle potential errors within the asynchronous callback, preventing unhandled rejections and ensuring graceful error handling.