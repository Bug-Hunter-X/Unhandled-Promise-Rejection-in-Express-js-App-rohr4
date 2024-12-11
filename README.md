# Unhandled Promise Rejection in Express.js
This repository demonstrates a common error in Node.js Express applications: unhandled promise rejections resulting from errors within asynchronous operations. The `bug.js` file shows an Express server that simulates an asynchronous task that might throw an error.  The error isn't properly caught, leading to the server crashing.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js`.
4. Observe the server's behavior.  The server will likely crash after a few requests. 
5. Then run `node bugSolution.js` and see that it handles errors gracefully.

## Solution
The issue stems from not using proper error handling within the asynchronous function.  The solution involves using a `try...catch` block to handle potential errors and providing appropriate responses to the client.