# Node.js Server Hanging Issue

This repository demonstrates a common issue in Node.js applications where long-running requests can cause the server to hang. The `server.js` file contains a simple HTTP server that simulates a 5-second delay on each request. This blocks the event loop, preventing the server from responding to further requests.

The solution, `serverSolution.js`, shows how to use asynchronous operations (e.g., `setTimeout`) to prevent blocking the event loop and improve server responsiveness.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node server.js`.
4. Open multiple tabs in your browser and try to access `http://localhost:3000`.  Observe the hanging behavior after a few requests. 
5. Run `node serverSolution.js` to see the improved responsiveness.

## Solution

The solution utilizes asynchronous programming techniques to handle long-running tasks without blocking the event loop.  This allows the server to remain responsive to other requests even when processing tasks that take a considerable amount of time.