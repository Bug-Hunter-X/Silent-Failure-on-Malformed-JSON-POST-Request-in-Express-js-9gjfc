# Silent Failure on Malformed JSON POST Request
This repository demonstrates a common issue in Express.js applications where malformed JSON data in POST requests leads to silent failures without proper error handling.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version.

## Problem
The original code lacks error handling for scenarios where the request body (`req.body`) is not properly parsed due to invalid JSON format. This results in a failure that isn't explicitly reported to the client, making debugging difficult.

## Solution
The solution incorporates error handling using a `try...catch` block to manage potential JSON parsing errors.  If parsing fails, an appropriate error response is sent to the client.