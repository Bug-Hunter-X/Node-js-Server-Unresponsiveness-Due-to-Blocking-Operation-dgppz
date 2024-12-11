# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running operation blocking the event loop.  The `server.js` file contains the buggy code, while `server-solution.js` provides a solution using asynchronous operations.

**Problem:** The original code executes a computationally intensive loop within the request handler. This blocks the event loop, causing the server to become unresponsive to new requests.  The server effectively hangs.

**Solution:** The solution uses asynchronous programming techniques (e.g., `setTimeout` for demonstration, but more robust solutions exist) to offload long-running tasks from the main event loop. This allows the server to remain responsive to other requests.