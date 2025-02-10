# Node.js Server Unresponsiveness Due to Long-Running Tasks

This repository demonstrates a common issue in Node.js server development: unresponsiveness caused by long-running operations within request handlers.  The example shows a server that introduces a 5-second delay.  While seemingly simple, this delay can lead to problems with scalability and responsiveness in production environments.

## Problem

The `server.js` file contains a Node.js HTTP server that simulates a long-running operation (a 5-second delay).  During this delay, the server is unresponsive to new requests. This can lead to poor user experience and potential application crashes.

## Solution

The `serverSolution.js` file provides an improved version of the server.  It utilizes asynchronous operations and proper error handling to prevent the server from becoming unresponsive.  This is crucial for handling numerous requests concurrently without blocking.

## How to Run

1. Clone the repository.
2. Navigate to the project directory.
3. Run `node server.js` for the problematic server.
4. Run `node serverSolution.js` for the improved server.